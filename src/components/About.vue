<script setup>
/*
    About.vue
    Author: Charlotte Soeurng
*/
const interests = [
    'Machine Learning',
    'Philosophy & Ethics',
    'Fitness',
    'Reading & Writing'
]

function scroll(id) {
    document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
    <section id="about" class="hero">
        <div class="hero-container">
            <div class="hero-text">
                <h1 class="hero-name">Charlotte Soeurng</h1>
                <p class="hero-title">
                    Software Developer &nbsp;·&nbsp; Minneapolis, MN
                </p>

                <div class="card about-card">
                    <p class="card-label">About Me</p>
                    <p class="card-text">
                        <strong>Software Developer</strong> with a focus on <strong>web application</strong> and <strong>full-stack development</strong>. Owned frontend development and UI/UX implementation for nonprofit crime resource directory, integrating search and filter functions for over 300 resources across Minnesota. Proficient in JavaScript, Java, Python, SQL, Vue.js, REST APIs and Machine Learning concepts.
                    </p>

                    <div class="why-hire">
                        <p class="card-label">Why hire me?</p>
                        <p class="card-text">
                            I ship real products for real people. I built and deployed a crime resource directory for crime victims across Minnesota that is currently deployed and used by client, advocates, and victims.
                            <br>I also founded 
                            <strong>foodscale, </strong>my own meal prep calculator that calculates exact protein grams and calories for lifters and strict dieters who meal prep with limited food set and macronutrient limits. The demo is currently finished, with the full version launching in July 2026.
                            <br>My 
                            <strong>philosophy </strong> background improves how I reason about user experience, allowing me to approach problems from ethical, logical, and philosophical perspectives.
                        </p>
                    </div>
                </div>

                <div class="details">
                    <span class="detail">
                        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M22 10v6M2 10l10-5 10 5-10 5z"/>
                            <path d="M6 12v5c3 3 9 3 12 0v-5"/>
                        </svg>
                        University of St. Thomas
                    </span>
                    <span class="detail">
                        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M22 10v6M2 10l10-5 10 5-10 5z"/>
                            <path d="M6 12v5c3 3 9 3 12 0v-5"/>
                        </svg>
                        Computer Science
                    </span>
                    <span class="detail">
                        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M22 10v6M2 10l10-5 10 5-10 5z"/>
                            <path d="M6 12v5c3 3 9 3 12 0v-5"/>
                        </svg>
                        Data Science Minor
                    </span>
                    <span class="detail">
                        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <rect x="3" y="4" width="18" height="18" rx="2"/>
                            <line x1="16" y1="2" x2="16" y2="6"/>
                            <line x1="8" y1="2" x2="8" y2="6"/>
                            <line x1="3" y1="10" x2="21" y2="10"/>
                        </svg>
                        Class of 2026
                    </span>
                </div>

                <div class="interests">
                    <span v-for="i in interests" :key="i" class="interest">{{ i }}</span>
                </div>

                <div class="links">
                    <a href="#resume" class="btn btn-primary" @click.prevent="scroll('resume')">
                        Resume
                    </a>
                    <a href="#projects" class="btn btn-secondary" @click.prevent="scroll('projects')">
                        Projects
                    </a>
                    <a
                        href="https://github.com/charlottesoeurng"
                        target="_blank"
                        rel="noopener"
                        class="btn btn-tertiary"
                    >
                        GitHub ↗
                    </a>
                </div>
            </div>

            <div class="picture">
                <div class="picture-wrap">
                    <img class="picture-headshot" src="/headshot.jpg" alt="Charlotte Soeurng" />
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/aboutStyle.css';
</style>

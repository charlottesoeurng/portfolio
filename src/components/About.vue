<script setup>
/*
    About.vue
    Author: Charlotte Soeurng
*/
const interests = [
    'Web Development',
    'Game Making',
    'Machine Learning',
    'Philosophy',
    'Reading / Writing'
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
                    Computer Science &nbsp;·&nbsp; St. Paul, MN
                </p>

                <div class="card about-card">
                    <p class="card-label">About Me</p>
                    <p class="card-text">
                        I am an upcoming computer science graduate from the University of St. Thomas with a passion for building impactful products to benefit the common good. I have strong interests in frontend development, UI design, and game development.
                    </p>

                    <div class="why-hire">
                        <p class="card-label">Why should you hire me?</p>
                        <p class="card-text">
                            I not only bring experience in
                            <strong>Software Development</strong> and
                            <strong>Data Science</strong>, but I also have a solid background in
                            <strong>Philosophy</strong>.
                            That allows me to improve my judgement and critical thinking skills as I approach issues from ethical, logical, and philosopical perspectives.
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

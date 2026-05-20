<script setup>
/*
    Skills.vue
    Author: Charlotte Soeurng
*/
const technical = [
    'Python',
    'JavaScript',
    'Java',
    'Vue.js',
    'HTML / CSS',
    'REST APIs',
    'Git / GitHub',
    'SQL',
    'Vue.js', 'Foundation (Framework)',
    'GameMaker Studio',
    'Data Mining',
    'Data Analysis',
    'Machine Learning',
    'Linux',
    'Agile / Scrum',
]

const professional = [
    'Project Management',
    'Problem Solving',
    'Cross-functional Collaboration',
    'Organization',
    'Critical Thinking',
    'Analytical Reasoning',
    'Attention to Detail',
    'Adaptability',
]
</script>

<template>
    <section id="skills" class="skills-section">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Skills</h2>
            </div>

            <div class="skills-grid">
                <div class="card skills-card">
                    <h3 class="col-heading">Technical Skills</h3>
                    <div class="tag-group">
                        <span
                            v-for="skill in technical"
                            :key="skill"
                            class="skill-tag"
                        >
                            {{ skill }}
                        </span>
                    </div>
                </div>

                <div class="card skills-card">
                    <h3 class="col-heading">Professional Competencies</h3>
                    <div class="tag-group">
                        <span
                            v-for="skill in professional"
                            :key="skill"
                            class="skill-tag soft"
                        >
                            {{ skill }}
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/skillsStyle.css';
</style>

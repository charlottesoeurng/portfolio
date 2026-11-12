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
    'Node.js',
    'Pandas',
    'REST APIs',
    'Git / GitHub',
    'SQL',
    'Data Analysis',
    'Machine Learning',
    'Linux',
    'Vercel',
    'Render'
]

const professional = [
    'Project Management',
    'Quality Assurance and Testing',
    'Cross-functional Collaboration',
    'Stakeholder Communication',
    'Technical Documentation',
    'Agile / Scrum'
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

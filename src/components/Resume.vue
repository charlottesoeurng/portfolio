<script setup>
/*
    Resume.vue
    Author: Charlotte Soeurng
*/
const RESUME_URL = `${import.meta.env.BASE_URL}resume.pdf`
</script>

<template>
    <section id="resume" class="resume-section">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Resume</h2>
            </div>

            <div class="resume-content">
                <div class="resume-actions">
                    <a :href="RESUME_URL" download="Charlotte_Soeurng_Resume.pdf" class="btn btn-primary">
                        ↓ Download Resume
                    </a>
                    <a :href="RESUME_URL" target="_blank" rel="noopener" class="btn btn-ghost">
                        Open Full Screen ↗
                    </a>
                </div>

                <div class="resume-embed card">
                    <iframe
                        :src="RESUME_URL"
                        title="Resume PDF"
                        class="resume-frame"
                        frameborder="0"
                    ></iframe>
                    <p class="resume-fallback">
                        PDF preview not supported in your browser.
                        <a :href="RESUME_URL" download>Download the PDF</a> to view it.
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/resumeStyle.css';
</style>

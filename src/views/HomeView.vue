<script setup>
/*
    HomeView.vue
    Author: Charlotte Soeurng
*/
import NavBar from '@/components/NavBar.vue'
import About from '@/components/About.vue'
import Skills from '@/components/Skills.vue'
import Projects from '@/components/Projects.vue'
import Resume from '@/components/Resume.vue'
</script>

<template>
    <div class="portfolio">
        <NavBar />
        <main>
            <About />
            <Skills />
            <Projects />
            <Resume />
        </main>
        <footer class="footer">
            <div class="footer-section">
                <p class="footer-texts">
                    © 2026 <strong>Charlotte Soeurng</strong>
                </p>
                <div class="footer-links">
                    <a href="https://github.com/charlotteSoeurng" target="_blank" rel="noopener">GitHub</a>
                    <a href="https://linkedin.com/in/CharlotteSoeurng" target="_blank" rel="noopener">LinkedIn</a>
                    <a href="mailto:charlottesoeurng@outlook.com">Email</a>
                </div>
            </div>
        </footer>
    </div>
</template>

<style>
    @import '../assets/homeStyle.css';
</style>

<script setup>
/*
    OtherView.vue
    Author: Charlotte Soeurng
*/
import NavBar from '@/components/NavBar.vue'
import Other from '@/components/Other.vue'
</script>

<template>
    <div class="portfolio">
        <NavBar />
        <main>
            <Other />
        </main>
        <footer class="footer">
            <div class="footer-section">
                <p class="footer-texts">
                    © 2026 <strong>Charlotte Soeurng</strong>
                </p>
                <div class="footer-links">
                    <a href="https://github.com/charlotteSoeurng" target="_blank" rel="noopener">GitHub</a>
                    <a href="https://linkedin.com/in/Charlotte-Soeurng" target="_blank" rel="noopener">LinkedIn</a>
                    <a href="mailto:charlottesoeurng@outlook.com">Email</a>
                </div>
            </div>
        </footer>
    </div>
</template>

<style>
    @import '../assets/homeStyle.css';
</style>

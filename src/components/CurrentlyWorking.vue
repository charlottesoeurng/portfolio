<script setup>
/*
    CurrentlyWorking.vue
    Author: Charlotte Soeurng
*/
const items = [
    {
        label: 'Building',
        title: 'foodscale',
        description: 'A meal prep calculator for lifters and strict dieters who work within a fixed food set and macro limits.',
        badge: 'Launching July 2026',
    },
    {
        label: 'Reading',
        title: 'Currently reading',
        description: '',
        badge: 'Psychological Thriller',
    },
]
</script>

<template>
    <section id="currently-working">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">What I'm Working On</h2>
            </div>

            <div class="cw-grid">
                <div v-for="item in items" :key="item.label" class="card cw-card">
                    <p class="cw-label">{{ item.label }}</p>
                    <h3 class="cw-title">{{ item.title }}</h3>
                    <p v-if="item.description" class="cw-description">{{ item.description }}</p>
                    <span class="cw-badge">{{ item.badge }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/currentlyWorkingStyle.css';
</style>

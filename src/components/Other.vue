<script setup>
/*
    Other.vue
    Author: Charlotte Soeurng
*/
const items = [
    {
        label: 'Building',
        title: 'FoodScale',
        description: 'Meal prep calculator for lifters and strict dieters utilizing within a fixed food set and macronutrient constraints.',
        badge: 'Launching August 2026',
    },
]
</script>

<template>
    <section id="currently-working">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">is currently working on...</h2>
            </div>

            <div class="cw-grid">
                <div v-for="item in items" :key="item.label" class="card cw-card">
                    <p class="cw-label">{{ item.label }}</p>
                    <h3 class="cw-title">{{ item.title }}</h3>
                    <p v-if="item.description" class="cw-description" v-html="item.description"></p>
                    <span class="cw-badge">{{ item.badge }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/other.css';
</style>

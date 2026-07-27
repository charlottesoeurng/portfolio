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
        badge: 'Launching July 2026',
    },
    {
        label: 'Reading',
        title: 'Sharp Objects',
        description: `
            Psychological thriller about a reporter investigating murders in her hometown. Fresh from a brief stay at a psych hospital, Camille Preaker returns to Wind Gap, Missouri, to report on the unsolved homicides of two girls.
            <br><br>
        `,
        badge: 'By Gillian Flynn',
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

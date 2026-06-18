<script setup>
/*
    OtherView.vue
    Author: Charlotte Soeurng
*/
import NavBar from '@/components/NavBar.vue'
import CurrentlyWorking from '@/components/CurrentlyWorking.vue'
</script>

<template>
    <div class="portfolio">
        <NavBar />
        <main>
            <CurrentlyWorking />
        </main>
    </div>
</template>

<style>
    @import '../assets/homeStyle.css';
</style>

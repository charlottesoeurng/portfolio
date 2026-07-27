<script setup>
/*
    NavBar.vue
    Author: Charlotte Soeurng
*/
import { ref, onMounted, onUnmounted } from 'vue'
import { RouterLink, useRouter, useRoute } from 'vue-router'

const router = useRouter()
const route = useRoute()

const isScrolled = ref(false)
const activeSection = ref('about')
const menuOpen = ref(false)

const menu = [
    { id: 'about',    label: 'About' },
    { id: 'skills',   label: 'Skills' },
    { id: 'projects', label: 'Projects' },
    { id: 'resume',   label: 'Resume' },
]

async function scrollTo(id) {
    menuOpen.value = false
    if (route.path !== '/') {
        await router.push('/')
        setTimeout(() => {
            document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
        }, 100)
    } else {
        document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
    }
}

function handleScroll() {
    isScrolled.value = window.scrollY > 20
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)

    const intersecting = new Set()
    const observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) intersecting.add(entry.target.id)
                else intersecting.delete(entry.target.id)
            })
            const top = menu.map(m => m.id).find(id => intersecting.has(id))
            if (top) activeSection.value = top
        },
        { rootMargin: '-20% 0px -70% 0px' }
    )

    menu.forEach(({ id }) => {
        const el = document.getElementById(id)
        if (el) observer.observe(el)
    })
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
    <nav :class="['navbar', { scrolled: isScrolled }]">
        <div class="nav-section">
            <a class="logo" href="#" @click.prevent="scrollTo('about')">
                Charlotte Soeurng
            </a>

            <ul class="nav-links" :class="{ open: menuOpen }">
                <li v-for="item in menu" :key="item.id">
                    <a
                        href="#"
                        :class="{ active: activeSection === item.id && route.path === '/' }"

                        @click.prevent="scrollTo(item.id)"
                    >
                        {{ item.label }}
                    </a>
                </li>
                <li>
                    <RouterLink to="/other" :class="{ active: route.path === '/other' }">Other</RouterLink>
                </li>
            </ul>

            <button
                class="hamburger"
                :class="{ open: menuOpen }"
                @click="menuOpen = !menuOpen"
                aria-label="Toggle menu"
            >
                <span></span><span></span><span></span>
            </button>
        </div>
    </nav>
</template>

<style src="../assets/navBarStyle.css"></style>

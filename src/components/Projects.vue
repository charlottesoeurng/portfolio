<script setup>
/*
    Projects.vue
    Author: Charlotte Soeurng
*/

const projects = [
    {
        id: 1,
        title: 'Minnesota Alliance on Crime',
        date: 'February 2026 - August 2026',
        figure: `${import.meta.env.BASE_URL}macWebsite.png`,
        contribution: 'Frontend Developer, UI/UX Designer, and QA',
        description: `
            Responsive directory that connects crime victims, advocates, and organizations to over 300 resources around the state. I owned every user-facing domain within an agile development environment. I built search and filter functionality, accessibility features, responsive design system, and conducted cross-browser and cross-device testing for every implementation front and back end. Fully responsible for the user experience, my design philosophy was to build safety measures for worst-case scenarios while ensuring the application was accessible to all users.
            <br><br>
            The application successfully launched in May 2026 and is currently live and used by nonprofits and crime victims. I updated and maintained the application until August 2026. 
            <br><br>
            (Map tiles are currently restricted due to a licensing issue)
            <br><br>
        `,
        keywords: ['Vue.js', 'JavaScript', 'LeafLet', 'Firebase', 'Web Application', 'Agile', 'Vercel'],
        links: [
            { label: 'Deployment', href: 'https://crime-resource-directory-mn.vercel.app/' },
        ],
    },
    {
        id: 2,
        title: 'FoodScale',
        date: 'June 2026 - Present',
        figure: `${import.meta.env.BASE_URL}foodscale.png`,
        contribution: 'Full Stack Engineer',
        description: `
            Meal prep calculator for weightlifters and strict dieters utilizing within a fixed food set and macronutrient constraints. Inputs ingredients, macro goals, and remaining meals. Outputs customized meal plans according to the user's specifications. I built the full stack application using an external API from USA Food Data Central, and designed algorithm using greedy approach and linear interpolation. I implemented responsive UI/UX and conducted all testing.
            <br><br>
            The MVP was launched in September 2026, and finished development in November 2026.
        `,
        keywords: ['Vue.js', 'JavaScript', 'USDA', 'Web Application', 'Render'],
        links: [
            { label: 'Deployment', href: 'https://foodscale.onrender.com/' },
        ],
    },
    {
        id: 3,
        title: 'GreenStep Cities',
        date: 'September 2025 - December 2025',
        figure: `${import.meta.env.BASE_URL}greenstep.png`,
        contribution: 'Database Developer',
        description: `
            Minnesota nonprofit requested a database for an application that tracks city sustainability initiatives all across the state. I implemented a relational database schema, built data structures and relationships, and created queries.
            <br><br>
            The database was used by the web development team to build an application that allows cities to track their sustainability initiatives and progress.
        `,
        keywords: ['MySQL', 'Database Design'],
        links: []
    }
]
</script>

<template>
    <section id="projects">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Software Engineering Experience</h2>
            </div>

            <div class="projects-grid">
                <article
                    v-for="project in projects"
                    :key="project.id"
                    class="card project-card"
                >
                    <div class="card-figure">
                        <img :src="project.figure" :alt="project.title" />
                    </div>

                    <div class="card-body">
                        <h3 class="card-title">{{ project.title }}</h3>

                        <p class="card-description">
                            {{ project.date }}
                        </p>

                        <p v-if="project.contribution" class="card-contribution">
                            <em>{{ project.contribution }}</em>
                        </p>

                        <div class="card-description" v-html="project.description"></div>

                        <div class="card-keywords">
                            <span v-for="kw in project.keywords" :key="kw" class="kw-tag">{{ kw }}</span>
                        </div>

                        <div v-if="project.links.length" class="card-links">
                            <a
                                v-for="link in project.links"
                                :key="link.label"
                                :href="link.href"
                                target="_blank"
                                rel="noopener"
                                class="card-link"
                            >
                                {{ link.label }} ↗
                            </a>
                        </div>
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>

<style>
    @import '../assets/projectsStyle.css';
</style>

<script setup>
/*
    Projects.vue
    Author: Charlotte Soeurng
*/

const projects = [
    {
        id: 1,
        title: 'Minnesota Alliance on Crime',
        date: 'February 2026 - July 2026',
        figure: `${import.meta.env.BASE_URL}macWebsite.png`,
        contribution: 'Frontend Developer, UI/UX Designer, and QA',
        description: `
            Minnesota nonprofit needed responsive directory to connect crime victims, advocates, and organizations to over 300 resources around the state. I owned frontend development, UI/UX design, and QA on a small team under a tight schedule. I built search and filter functionality, dark mode, responsive design system, and conducted cross-browser and cross-device testing for every implementation front and back end.
            <br><br>
            The directory successfully launched by the end of May 2026, and is currently live and used by nonprofits and crime victims.
            <br><br>
        `,
        keywords: ['Vue.js', 'JavaScript', 'LeafLet', 'Firebase', 'API', 'Crime Resources', 'Web Application', 'NonProfit'],
        links: [
            { label: 'Deployment', href: 'https://crime-resource-directory-mn.vercel.app/' },
        ],
    },
    {
        id: 2,
        title: 'FoodScale',
        date: 'May 2026 - Present',
        figure: `${import.meta.env.BASE_URL}foodscale.png`,
        contribution: 'Founder, Developer, and Designer',
        description: `
            Meal prep calculator for lifters and strict dieters utilizing within a fixed food set and macronutrient constraints. I built the full stack application, including frontend, and backend using the USA Food Data Central API. I also designed responsive UI/UX and conducted all testing.
            <br><br>
            The demo is currently finished, with the full version launching in July 2026.
        `,
        keywords: ['Vue.js', 'JavaScript', 'USDA', 'Meal Prep Calculator', 'Web Application'],
        links: [],
    },
    {
        id: 3,
        title: 'GreenStep Cities',
        date: 'September 2025 - December 2025',
        figure: `${import.meta.env.BASE_URL}greenstep.png`,
        contribution: 'Database Developer',
        description: `
            Minnesota nonprofit needed a database for an application that tracks city sustainability initiatives all across the state. I implemented a relational database schema, built data structures and relationships, and created queries.
            <br><br>
            The database was used by the web development team to build an application that allows cities to track their sustainability initiatives and progress.
        `,
        keywords: ['SQL', 'MySQL', 'Database Design', 'Sustainability Tracker', 'NonProfit'],
        links: []
    },
    {
        id: 4,
        title: 'Indigo Water',
        date: 'November 2024 - May 2025',
        figure: `${import.meta.env.BASE_URL}indigoWater.png`,
        contribution: 'Programmer, Level Designer',
        description: `
            Assembled team to build a complete 2D fishing game that focuses on recycling. I owned programming and level design, implementing every system such as player movement, collision, inventory, and a crafting mechanic that allows players to combine collected garbage into reusable items.
            <br><br>
            The game was released on itch.io and is available for free, online play on Windows.
        `,
        keywords: ['GameMaker', 'Game Development', '2D Game', 'Fishing', 'Recycling'],
        links: [
            { label: 'Play', href: 'https://soregunned.itch.io/indigo-water' },
        ],
    },
    {
        id: 5,
        title: 'Book Club',
        date: 'September 2024 - December 2024',
        figure: `${import.meta.env.BASE_URL}theaterProduction.png`,
        contribution: 'Props and Lighting Technician',
        description: `
            Theater Performance class had a public performance for Book Club, adapted from an existing piece. I managed props for a 12-person cast, sourcing books and additional items from campus resources. I also ran all lighting during the 60-minute performance, supporting every rehearsal and the final live show at the end of the semester.
            <br><br>
            The performance was a success. It had a full house with seats occupied by both the campus and the local community, and it also sparked a genuine interest in theater that I didn't have when I first joined the team.
        `,
        keywords: ['Theater', 'Backstage', 'Live Performance', 'Props', 'Lighting'],
        links: [],
    },
]
</script>

<template>
    <section id="projects">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Projects and Experiences</h2>
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

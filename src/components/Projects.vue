<script setup>
/*
    Projects.vue
    Author: Charlotte Soeurng
*/
const projects = [
    {
        id: 1,
        title: 'Minnesota Alliance on Crime',
        figure: `${import.meta.env.BASE_URL}macWebsite.png`,
        contribution: 'Lead Frontend Developer, UI Designer, and QA',
        description: `
            <strong>Situation:</strong> Developed mobile-responsive crime resource directory for nonprofits and Minnesota crime victims.
            <br><br>
            <strong>Obstacle:</strong> Small team with tight schedules, and navigating real-world client needs and expectations. 
            <br><br>
            <strong>Action:</strong> Led frontend development using Vue.js, created design system and dark mode features, and tested all implementations (frontend, backend) across different devices and browsers.
            <br><br>
            <strong>Result:</strong> Successfully launched directory with positive client feedback, and learned how to balance technical decisions with user needs and project constraints.
        `,
        keywords: ['Vue.js', 'SQL', 'Web Development'],
        links: [
            { label: 'GitHub', href: 'https://github.com/JesseBA04/sp26-team3-mac' },
        ],
    },
    {
        id: 2,
        title: 'Indigo Water',
        figure: `${import.meta.env.BASE_URL}indogoWater.png`,
        contribution: 'Programmer and Level Designer',
        description: `
            <strong>Situation:</strong> Built a 2D fishing game using GameMaker. The player drives a boat, collects fish, and occasionally pulls up trash, which can be combined to craft reusable items.
            <br><br>
            <strong>Obstacle:</strong> Working solo as the programmer meant owning every system: player movement, collision, inventory, and the crafting mechanic. Scoping a complete, playable game within a semester was the main challenge.
            <br><br>
            <strong>Action:</strong> Implemented all gameplay systems in GameMaker, including boat controls, fish and trash spawning, and a crafting system that lets players build new items from collected garbage.
            <br><br>
            <strong>Result:</strong> Shipped a playable game and published it on itch.io. It was my first experience taking a game from concept to a live release.
        `,
        keywords: ['GameMaker', 'itch.io', 'Game Development'],
        links: [
            { label: 'itch.io', href: 'https://soregunned.itch.io/indigo-water' },
        ],
    },
    {
        id: 3,
        title: 'Cadenci: Music Recommendation',
        figure: `${import.meta.env.BASE_URL}cadenci.png`,
        contribution: 'Developer',
        description: `
            <strong>What I was trying to do:</strong> Designed Cadenci as a fun personal project, a music recommendation web app that suggests songs based on their opening lines. I completed the full frontend development and filled the database with an initial set of songs before the project stalled.
            <br><br>
            <strong>What didn't go as planned:</strong> I ran into copyright issues around licensing and displaying song lyrics, which made the idea practically impossible to continue due to legal constraints. I stopped the development before it could be completed.
            <br><br>
            <strong>What I learned & do differently now:</strong> I learned to do intensive research on legal and licensing considerations before starting any project, and to be more mindful of potential ethical and legal implications of the work I create.
        `,
        keywords: ['JavaScript', 'SQL', 'Web Development'],
        links: [],
    },
    {
        id: 4,
        title: 'The Culture of Front Doors',
        figure: `${import.meta.env.BASE_URL}frontDoor.png`,
        contribution: 'Writer and Researcher',
        description: `
            Wrote a research paper exploring what front doors reveal about the people who utilize them. Through specific hardware like material, door location, color choices, and glass panels, the paper argues that an everyday overlooked object carries deep cultural and personal meaning.
            <br><br>
            The paper recieved perfect scores and gave me a new perspective on design and user experience. I learned to look for the "why" behind design decisions, and to consider how even small details can communicate identity, values, and intent to users.
            <br><br>
            In the same way front doors signal identity and values, I learned to critically reflect on how my own work and design choices communicate who I am and what I stand for as a designer and developer.
        `,
        keywords: ['Cultural Studies', 'Research', 'Design'],
        links: [],
    },
    {
        id: 5,
        title: 'Book Club Production',
        figure: `${import.meta.env.BASE_URL}theaterProduction.png`,
        contribution: 'Props and Lighting Technician',
        description: `
            Served as props and lighting technician for <em>Book Club</em>, a class theater performance adapted from an existing play and open to the public. I supported both rehearsals throughout the semester and the final live performance, managing props and operating lights in real time.
            <br><br>
            The experience taught me how to stay focused and reliable under pressure. Even the smallest mistakes are visible to the audience, so precision and communication with the crew were absolutely essential.
            <br><br>
            Contributing to a public performance that brought the community together reflects the kind of work I find meaningful: collaborative, service-oriented, and inclusive. It also sparked a genuine interest in theater that I hadn't expected going in.
        `,
        keywords: ['Theater', 'Collaboration', 'Live Production'],
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

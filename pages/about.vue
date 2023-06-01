<template>
    <div class="about-page">
        <h3 class="text-highlight">About Me</h3>
        <h4>What I Do</h4>
        <div class="about-content">
            <div class="column">
                <img class="about-img" src="assets/headshot.webp" alt="Tyler Garner headshot">
                <ul class="skills-container">
                    <li class="skill">
                        <img class="skill-img" src="https://cdn.worldvectorlogo.com/logos/typescript.svg" alt="TypeScript logo">
                        <p class="skill-label">TypeScript</p>
                    </li>
                    <li class="skill">
                        <img class="skill-img" src="https://cdn.worldvectorlogo.com/logos/vue-9.svg" alt="Vue.js logo">
                        <p class="skill-label">Vue.js</p>
                    </li>
                    <li class="skill">
                        <img class="skill-img" src="https://cdn.worldvectorlogo.com/logos/nuxt-2.svg" alt="Nuxt logo">
                        <p class="skill-label">Nuxt</p>
                    </li>
                    <li class="skill">
                        <img class="skill-img" src="https://seeklogo.com/images/S/supabase-logo-DCC676FFE2-seeklogo.com.png" alt="Supabase logo">
                        <p class="skill-label">Supabase</p>
                    </li>
                </ul>
            </div>
            <div class="about-paragraphs">
                <p><span class="text-highlight first-letter">I</span> am a web developer from Gainesville, Texas, and I specialize in designing and developing websites for small businesses and organizations looking to establish a strong online presence. With over 5 years of web development experience, I am proficient in delivering visually-appealing and highly-performant websites.</p>
                <p>I have progressed my programming experience since 2017 when I graduated high school, and in 2020, I earned a Certificate in Web Development from Glendale Community College. To this day, I continue to learn new technologies and design patterns that benefit me the most in developing complex websites and applications.</p>
                <p>Having previously worked for Runway Proptech, I am experienced in developing multiple websites for clients in the United States and Australia, and ensuring the designs and functionality perfectly fit the clients' visions.</p>
                <p>Being front-end focused, I develop static websites by hand, or with Vue.js and Nuxt, depending on the level of interactivity required by the project. For backend code and databases, I utilize Supabase as an open-source, quick and secure solution for developing full-stack websites and applications.</p>
                <p>I am always eager for new challenges and opportunities to demonstrate my proficiency in web development, so if you have any questions, or are interested in working with me, contact me today!</p>
                <NuxtLink to="/contact" class="button button-primary">Contact</NuxtLink>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        .about-page {
            min-height: 100vh;
            margin-top: 120px;
            padding: 0 var(--mobile-x-padding);
            h3, h4 {
                text-align: center;
            }
            .about-content {
                margin-top: 10rem;
            }
            .column {
                display: flex;
                flex-direction: column;
                gap: 3rem;
            }
            .about-img {
                filter: grayscale(1);
                width: 100%;
                box-shadow: var(--box-shadow);
            }
            .skills-container {
                display: none;
            }
            .skill {
                display: flex;
                flex-direction: row;
                align-items: center;
                gap: 2rem;
            }
            .skill-img {
                width: 50px;
            }
            .skill-label {
                color: var(--color-black);
            }
            .about-paragraphs {
                margin-top: 5rem;
                display: flex;
                flex-direction: column;
                gap: 3rem;
            }
            .first-letter {
                font-family: 'Roboto Condensed', sans-serif;
                font-weight: bold;
                font-size: 6rem;
                line-height: 20px;
            }
        }
    }
    @media screen and (min-width: 768px) {
        .about-page {
            padding: 0 var(--tablet-x-padding);
            .about-content {
                display: flex;
                flex-direction: row;
                gap: 5rem;
            }
            .about-img {
                width: 250px;
                height: 250px;
            }
            .about-paragraphs {
                width: 450px;
                margin: 0;
                position: relative;
                top: 7px;
            }
            .skills-container {
                background-color: var(--color-white);
                box-shadow: var(--box-shadow);
                padding: 2rem;
                display: flex;
                flex-direction: column;
                gap: 2rem;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        .about-page {
            padding: 0 var(--desktop-x-padding);
            .about-img {
                width: 350px;
                height: 350px;
            }
            .about-paragraphs {
                top: 16px;
                width: auto;
            }
        }
    }
    @media screen and (min-width: 1920px) {
        .about-page {
            padding: 0 var(--widescreen-x-padding);
        }
    }
</style>
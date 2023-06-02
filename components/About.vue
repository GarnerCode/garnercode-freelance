<template>
    <section id="about">
        <div class="section-header">
            <h3>About Me</h3>
            <h4>What I Do</h4>
        </div>
        <div class="about-content">
            <img class="about-img" src="assets/headshot.webp" alt="Tyler Garner headshot">
            <div class="paragraphs">
                <p class="about-text">
                    <span class="text-highlight first-letter">M</span>y name is Tyler Garner, and I'm a freelance web developer from Gainesville, Texas. With over 5 years of experience, I am skilled in delivering optimized websites with top-notch performance across any device.
                </p>
                <p class="about-text">
                    I specialize in developing custom websites for small businesses and organizations that are looking to establish a strong online presence. With a keen eye for design and a passion for coding, I strive to deliver visually appealing and highly functional websites that cater to the unique needs of my clients.
                </p>
                <button class="button button-primary">More About Me</button>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #about {
            padding: 0 var(--mobile-x-padding);
            .section-header {
                margin-bottom: 10rem;
            }
            .about-content {
                display: flex;
                flex-direction: column;
                gap: 5rem;
            }
            .about-img {
                width: 100%;
                filter:grayscale(1);
                box-shadow: var(--box-shadow);
            }
            .paragraphs {
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
        #about {
            padding: 0 var(--tablet-x-padding);
            .about-content {
                flex-direction: row;
            }
            .about-img {
                width: 250px;
                height: 250px;
            }
            .paragraphs {
                position: relative;
                top: 7px;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #about {
            padding: 0 var(--desktop-x-padding);
            .about-img {
                width: 350px;
                height: 350px;
            }
            .paragraphs {
                top: 12px;
            }
        }
    }
    @media screen and (min-width: 1920px) {
        #about {
            padding: 0 var(--widescreen-x-padding);
            .paragraphs {
                top: 16px;
            }
        }
    }
</style>
<template>
    <section id="services">
        <div class="section-header">
            <h3>My Services</h3>
            <h4>Services I offer</h4>
        </div>
        <div class="services-container flex-column gap-10">
            <div class="service">
                <div class="icon-container">
                    <img class="service-icon" src="assets/icon-design.svg" alt="">
                </div>
                <div class="service-text flex-column gap-1">
                    <h5 class="service-title">Design</h5>
                    <p class="service-description">Your website is the face of your business, so I meticulously design websites so that they stand out from the competition and attract potential customers!</p>
                </div>
            </div>
            <div class="service">
                <div class="icon-container">
                    <img class="service-icon" src="assets/icon-develop.svg" alt="">
                </div>
                <div class="service-text flex-column gap-1">
                    <h5 class="service-title">Development</h5>
                    <p class="service-description">With a focus in SEO and performance, I use every tool at my disposal to ensure users discover your website and stick around to become future customers!</p>
                </div>
            </div>
            <div class="service">
                <div class="icon-container">
                    <img class="service-icon" src="assets/icon-hosting.svg" alt="">
                </div>
                <div class="service-text flex-column gap-1">
                    <h5 class="service-title">Deploy</h5>
                    <p class="service-description">Take the guess-work out of deploying your website by allowing a professional to setup hosting and domains, so that you can focus on growing your business!</p>
                </div>
            </div>
        </div>
        <NuxtLink to="/services" class="button button-primary">Learn More</NuxtLink>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #services {
            padding: 5rem var(--mobile-x-padding);
            padding-bottom: 0;
            .section-header {
                margin-bottom: calc(10rem + 50px);
            }
            .service {
                padding: 0 var(--mobile-x-padding);
            }
            .icon-container {
                background-color: var(--color-primary);
                width: 100px;
                height: 100px;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                margin: 0 auto;
                position: relative;
                top: -50px;
                transform: rotate(45deg);
                img {
                    transform: rotate(-45deg);
                }
            }
            .service-icon {
                width: 60px;
            }
            .service-text {
                position: relative;
                top: -25px;
                text-align: center;
            }
            .service-title {
                text-align: center;
            }
            .button {
                margin: 0 auto;
                margin-top: 5rem;
            }
        }
    }
    @media screen and (min-width: 768px) {
        #services {
            padding: 5rem var(--tablet-x-padding);
            padding-bottom: 0;
            .services-container {
                align-items: center;
            }
            .service {
                width: 300px;
            }
            button {
                margin: 0 auto;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #services {
            padding: 5rem var(--desktop-x-padding);
            padding-bottom: 0;
            .services-container {
                flex-direction: row;
                justify-content: space-between;
            }
        }
    }
    @media screen and (min-width: 1920px) {
        #services {
            padding: 5rem var(--widescreen-x-padding);
            padding-bottom: 0;
        }
    }
</style>
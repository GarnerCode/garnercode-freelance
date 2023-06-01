<template>
    <div class="services-page">
        <h3 class="text-highlight">My Services</h3>
        <h4>Services I Offer</h4>
        <div class="services-content">
            <div class="service">
                <img class="service-icon service-icon-tablet" src="assets/design.svg" alt="">
                <div class="service-text">
                    <div class="service-header">
                        <img class="service-icon service-icon-mobile" src="assets/design.svg" alt="">
                        <div class="service-title">Design</div>
                        <div class="header-bar"></div>
                    </div>
                    <div class="service-details">
                        <p>Great web design is a key factor in a user's initial impression of a business. Is it professional? Is it easy to navigate? Does it display correctly across multiple devices?</p>
                        <p>Before development, I design mockups of websites to create the structure and style of the project, ensuring the finalized design is both professional, and is exactly how the client wants their website to look!</p>
                    </div>
                </div>
            </div>
            <div class="service">
                <div class="service-text">
                    <div class="service-header alt-header">
                        <div class="header-bar"></div>
                        <div class="service-title">Develop</div>
                        <img class="service-icon service-icon-mobile" src="assets/develop.svg" alt="">
                    </div>
                    <div class="service-details">
                        <p>SEO is another critical factor in determing if potential customers discover your website on Google. When they arrive, however, statistics show that roughly 40% of website visitors leave if the page takes longer than 3 seconds to load.</p>
                        <p>When developing websites, I focus on SEO and performance speed to ensure potential customers are more likely to visit your website, and stick around long enough to learn all about you and your business!</p>
                    </div>
                </div>
                <img class="service-icon service-icon-tablet" src="assets/develop.svg" alt="">
            </div>
            <div class="service">
                <img class="service-icon service-icon-tablet" src="assets/hosting.svg" alt="">
                <div class="service-text">
                    <div class="service-header">
                        <img class="service-icon service-icon-mobile" src="assets/hosting.svg" alt="">
                        <div class="service-title">Deploy</div>
                        <div class="header-bar"></div>
                    </div>
                    <div class="service-details">
                        <p>Deploying your website to a host server and attaching a unique domain name can be a confusing process. Why not let a professional handle the final steps to launching your new website?</p>
                        <p>I will setup your hosting and domain name, as well as walk you through the process of transferring ownership and billing in order to finalize the process!</p>
                    </div>
                </div>
            </div>
            <div class="service-contact">
                <p>If you have any questions, or are interested in working with me, contact me today!</p>
                <NuxtLink to="/contact" class="button button-primary">Contact</NuxtLink>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        .services-page {
            min-height: 100vh;
            margin-top: 120px;
            padding: 0 var(--mobile-x-padding);
            h3, h4 {
                text-align: center;
            }
            .services-content {
                margin-top: 10rem;
                display: flex;
                flex-direction: column;
                gap: 10rem;
            }
            .service-header {
                display: flex;
                flex-direction: row;
                gap: 5rem;
                align-items: center;
                &.alt-header {
                    justify-content: flex-end;
                }
            }
            .header-bar {
                display: none;
            }
            .service-icon {
                width: 150px;
                &.service-icon-tablet {
                    display: none;
                }
            }
            .service-title {
                font-family: 'Roboto Condensed', sans-serif;
                font-size: 30px;
                font-weight: bold;
                text-transform: uppercase;
                color: var(--color-primary);
            }
            .service-details {
                margin-top: 3rem;
                display: flex;
                flex-direction: column;
                gap: 3rem;
            }
            .service-contact {
                .button {
                    margin-top: 3rem;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        .services-page {
            padding: 0 var(--tablet-x-padding);
            .service {
                display: flex;
                flex-direction: row;
                gap: 3rem;
            }
            .header-bar {
                display: block;
                height: 1px;
                width: 100%;
                background-color: var(--color-white);
            }
            .service-icon {
                &.service-icon-mobile {
                    display: none;
                }
                &.service-icon-tablet {
                    display: block;
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        .services-page {
            padding: 0 var(--desktop-x-padding);
        }
    }
    @media screen and (min-width: 1920px) {
        .services-page {
            padding: 0 var(--widescreen-x-padding);
        }
    }
</style>
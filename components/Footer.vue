<template>
    <footer>
        <div class="footer-main">
            <div class="column">
                <div class="logo">Tyler Garner</div>
                <div class="email">tyler@garnercode.io</div>
            </div>
            <div class="column">
                <div class="column-title">Services</div>
                <div class="service">Web Design</div>
                <div class="service">Web Development</div>
                <div class="service">SEO Services</div>
                <div class="service">Hosting Setup</div>
            </div>
            <div class="column">
                <div class="column-title">Navigation</div>
                <NuxtLink v-for="(nav, index) of navData" :key="index" :to="nav.route">{{ nav.label }}</NuxtLink>
            </div>
        </div>
        <div class="copyright">Copyright © 2023 | Tyler Garner</div>
    </footer>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        footer {
            background-color: var(--color-white);
            padding: 5rem var(--mobile-x-padding);
            padding-bottom: 1rem;
            .footer-main {
                display: flex;
                flex-direction: column;
                gap: 3rem;
            }
            .logo {
                font-family: 'Roboto Condensed', sans-serif;
                font-size: 30px;
                font-weight: bold;
                text-transform: uppercase;
                color: var(--color-primary);
            }
            .email {
                font-size: 18px;
                font-style: italic;
            }
            .column {
                display: flex;
                flex-direction: column;
                gap: 2rem;
                a, .service {
                    text-decoration: none;
                    font-family: 'Roboto Condensed', sans-serif;
                    color: var(--color-black);
                    font-size: 18px;
                }
                a {
                    width: fit-content;
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
            }
            .column-title {
                font-family: 'Roboto Condensed', sans-serif;
                text-transform: uppercase;
                color: var(--color-black);
                font-size: 24px;
                font-weight: bold;
                text-transform: uppercase;
                border-bottom: 1px solid var(--color-primary);
                padding-bottom: 1rem;
            }
            .copyright {
                text-align: center;
                font-size: 12px;
                margin-top: 2rem;
            }
        }
    }
    @media screen and (min-width: 768px) {
        footer {
            padding: 5rem var(--tablet-x-padding);
            padding-bottom: 1rem;
            .footer-main {
                flex-direction: row;
                justify-content: space-between;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        footer {
            padding: 5rem var(--desktop-x-padding);
            padding-bottom: 1rem;
        }
    }
    @media screen and (min-width: 1920px) {
        footer {
            padding: 5rem var(--widescreen-x-padding);
            padding-bottom: 1rem;
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { navData } from '~/const/navData';

    export default defineComponent({
        name: 'Footer',
        data: () => {
            return {
                navData,
            }
        }
    })
</script>
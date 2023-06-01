<template>
    <div class="header-container">
        <header :class="{'alt-bg': $route.fullPath !== '/'}">
            <!-- <Logo></Logo> -->
            <div class="logo">
                <NuxtLink to="/" class="logo-text">
                    Tyler Garner
                </NuxtLink>
            </div>
            <div @click="navToggled = !navToggled" :class="{'toggled': navToggled}" class="mobile-nav-toggle">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
            <div v-if="navToggled" class="mobile-nav-container flex-column gap-5" :class="{'alt-bg': $route.fullPath !== '/'}">
                <div @click="navToggled = false" class="nav-item" v-for="(nav, index) of navItems" :key="index">
                    <div class="active-bar" :class="{'active': $route.fullPath === nav.route}"></div>
                    <NuxtLink :to="nav.route">{{ nav.label }}</NuxtLink>
                </div>
            </div>
            <div class="nav-container flex-row gap-3">
                <div class="nav-item" :class="{'active': $route.fullPath === nav.route}" v-for="(nav, index) of navItems" :key="index">
                    <NuxtLink :to="nav.route">{{ nav.label }}</NuxtLink>
                </div>
            </div>
        </header>
        <div v-if="navToggled" class="mobile-nav-overlay"></div>
    </div>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        .mobile-nav-overlay {
            position: absolute;
            top: 0;
            left: 0;
            z-index: 11;
            width: 100vw;
            height: 100vh;
            background-color: rgba(0,0,0,0.25);
            backdrop-filter: blur(5px);
        }
        header {
            padding: 0 var(--mobile-x-padding);
            width: calc(100vw - 6rem);
            height: 70px;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 12;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            background-color: var(--color-white);
            &.alt-bg {
                background-color: #fff;
            }
            .logo {
                // width: 200px;
                .logo-text {
                    font-size: 30px;
                    font-family: 'Roboto Condensed', sans-serif;
                    text-transform: uppercase;
                    font-weight: bold;
                    color: var(--color-black);
                    transition: var(--transition);
                    text-decoration: none;
                    cursor: pointer;
                    .logo-small {
                        width: 30px;
                    }
                    &:hover {
                        color: var(--color-primary);
                    }
                }
            }
            .mobile-nav-toggle {
                cursor: pointer;
                div {
                    width: 25px;
                    height: 3px;
                    background-color: var(--color-black);
                    margin: 5px;
                    transition: var(--transition);
                }
                &.toggled {
                    div {
                        background-color: var(--color-primary);
                    }
                    .line1 {
                        transform: rotate(-45deg) translate(-5px, 6px);
                    }
                    .line2 {
                        opacity: 0;
                    }
                    .line3 {
                        transform: rotate(45deg) translate(-5px, -6px);
                    }
                }
            }
            .nav-container {
                display: none;
            }
            .mobile-nav-container {
                position: absolute;
                z-index: 12;
                top: 70px;
                right: 0;
                background-color: var(--color-white);
                padding: 3rem;
                &.alt-bg {
                    background-color: #fff;
                }
                .nav-item {
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    gap: 1rem;
                    .active-bar {
                        width: 30px;
                        height: 3px;
                        background-color: var(--color-primary);
                        opacity: 0;
                        &.active {
                            opacity: 1;
                        }
                    }
                    a {
                        text-decoration: none;
                        color: var(--color-black);
                        font-family: 'Roboto Condensed', sans-serif;
                        font-weight: bold;
                        font-size: 30px;
                        text-transform: uppercase;
                    }
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        header {
            padding: 0 var(--tablet-x-padding);
            width: calc(100vw - 12rem);
            .mobile-nav-toggle {
                display: none;
            }
            .nav-container {
                display: flex;
            }
            .nav-item {
                a {
                    text-decoration: none;
                    font-family: 'Roboto Condensed', sans-serif;
                    color: var(--color-black);
                    text-transform: uppercase;
                    font-size: 18px;
                    transition: var(--transition);
                    &:hover {
                        color: var(--color-primary);
                    }
                }
                &.active {
                    border-bottom: 3px solid var(--color-primary);
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        header {
            padding: 0 var(--desktop-x-padding);
            width: calc(100vw - 40rem);
        }
    }
    @media screen and (min-width: 1920px) {
        header {
            padding: 0 var(--widescreen-x-padding);
            width: calc(100vw - 60rem);
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { navData } from '~/const/navData';

    export default defineComponent({
        name: 'Header',
        data: () => {
            return {
                navItems: navData,
                navToggled: false,
            }
        },
    })
</script>
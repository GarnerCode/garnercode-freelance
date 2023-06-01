<template>
    <section id="portfolio">
        <div class="section-header">
            <h3>My Portfolio</h3>
            <h4>{{ subtitle }}</h4>
        </div>
        <div class="portfolio-content">
            <div class="project" :class="{'alt': index % 2}" v-for="(project, index) of projects" :key="index">
                <img class="project-img" :src="project.imageUrl" :alt="`${project.title} thumbnail`">
                <div class="project-details">
                    <div class="project-title">{{ project.title }}</div>
                    <p class="project-description">{{ project.description }}</p>
                    <a :href="project.liveUrl" target="_blank" class="button button-primary">Visit Site</a>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #portfolio {
            padding: 5rem var(--mobile-x-padding);
            .portfolio-content {
                display: flex;
                flex-direction: column;
                gap: 5rem;
                margin-top: 10rem;
            }
            .project {
                .project-img {
                    width: 100%;
                    box-shadow: var(--box-shadow);
                }
                .project-details {
                    display: flex;
                    flex-direction: column;
                    gap: 2rem;
                }
                .project-title {
                    font-size: 30px;
                    font-family: 'Roboto Condensed', sans-serif;
                    font-weight: bold;
                    text-transform: uppercase;
                    margin-top: 1rem;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #portfolio {
            padding: 5rem var(--tablet-x-padding);
            .portfolio-content {
                gap: 0;
            }
            .project {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                padding: 5rem 0;
                &.alt {
                    flex-direction: row-reverse;
                    border-top: 1px solid var(--color-white);
                    border-bottom: 1px solid var(--color-white);
                }
                .project-img {
                    width: calc(50% - 2.5rem);
                }
                .project-details {
                    width: calc(50% - 2.5rem);
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #portfolio {
            padding: 5rem var(--desktop-x-padding);
            .project {
                .project-img {
                    width: calc(40% - 2.5rem);
                }
                .project-details {
                    width: calc(60% - 2.5rem);
                }
            }
        }
    }
    @media screen and (min-width: 1920px) {
        #portfolio {
            padding: 5rem var(--widescreen-x-padding);
        }
    }
</style>

<script lang="ts">
    import { defineComponent } from 'vue';
    import { projectData, featured } from '~/const/projectData';

    export default defineComponent({
        name: 'Portfolio',
        data: () => {
            return {
                projects: [] as any,
            }
        },
        props: {
            subtitle: {
                type: String
            },
            featured: {
                type: Boolean,
            }
        },
        mounted() {
            if (this.featured) {
                this.projects = featured;
            } else {
                this.projects = projectData;
            }
        }
    })
</script>
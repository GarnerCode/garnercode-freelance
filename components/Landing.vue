<template>
    <section id="landing">
        <div class="landing-text">
            <h1>Small Business</h1>
            <h2 class="subhead-top">Web Design</h2>
            <div class="flex-row center-x gap-2 subhead-bottom">
                <div class="landing-bar"></div>
                <h2>& Development</h2>
            </div>
            <p>I'm a freelance web developer that builds online platforms for small businesses and organizations.</p>
            <button class="button button-primary">Contact</button>
        </div>
        <img class="landing-hero" src="assets/landing-hero.webp" alt="Macbook displaying Arch project">
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #landing {
            background-color: var(--color-white);
            height: 100vh;
            padding: 0 var(--mobile-x-padding);
            display: flex;
            flex-direction: column;
            justify-content: center;
            .landing-bar {
                height: 3px;
                width: 30px;
                background-color: var(--color-primary);
            }
            p {
                margin: 3rem 0;
            }
            .landing-hero {
                display: none;
            }
        }
    }
    @media screen and (min-width: 768px) {
        #landing {
            padding: 0 var(--tablet-x-padding);
            height: calc(100vh + 110px);
            .landing-text {
                position: relative;
                bottom: 110px;
            }
            p {
                width: 450px;
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #landing {
            padding: 0 var(--desktop-x-padding);
            .landing-text {
                position: relative;
                z-index: 8;
            }
            .landing-hero {
                display: block;
                width: 500px;
                position: absolute;
                top: 250px;
                right: 20rem;
            }
        }
    }
    @media screen and (min-width: 1920px) {
        #landing {
            padding: 0 var(--widescreen-x-padding);
            .landing-hero {
                right: 30rem;
                width: 600px;
            }
        }
    }
</style>
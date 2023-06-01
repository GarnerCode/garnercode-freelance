<template>
    <div id="layout">
        <Header></Header>
        <main>
            <Nuxt />
        </main>
        <Footer></Footer>
    </div>
</template>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Roboto&family=Roboto+Condensed:wght@700&display=swap');
    :root {
        --color-black: #020A15;
        --color-white: #E6E6E6;
        --color-primary: #c5242a;
        --box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.25);
        --transition: all ease 0.25s;
        --mobile-x-padding: 3rem;
        --tablet-x-padding: 6rem;
        --desktop-x-padding: 20rem;
        --widescreen-x-padding: 30rem;
    }
    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
    * {
        font-family: 'Roboto', sans-serif;
        color: var(--color-black);
    }
    html {
        overflow-x: hidden;
        font-size: 62.5%;
        @media screen and (min-width: 112.5em) {
            font-size: 75%;
        }
        
        @media screen and (min-width: 85.375em) and (max-width: 75em) {
            font-size: 56.25%;
        }
        
        @media screen and (max-width: 56.25em) {
            font-size: 50%;
        }
        
        @media screen and (max-width: 28.125em) {
            font-size: 45%;
        }
    }
    ::-webkit-scrollbar {
        width: 10px;
    }
    ::-webkit-scrollbar-track {
        background: var(--color-white);
    }
    ::-webkit-scrollbar-thumb {
        background: var(--color-black);
    }
    .slide-enter, .slide-leave-to {
        opacity: 0;
        transform: translateY(-2rem);
    }
    .slide-enter-active, .slide-leave-active {
        transition: var(--transition);
    }
    .fade-enter, .fade-leave-to {
        opacity: 0;
    }
    .fade-enter-active, .fade-leave-active {
        transition: var(--transition);
    }
    body {
        margin: 0;
    }
    main {
        padding-bottom: 10rem;
    }
    h1, h2, h3, h4, h5 {
        font-family: 'Roboto Condensed', sans-serif;
        text-transform: uppercase;
        font-weight: bold;
        margin: 0;
        span {
            font-family: 'Roboto Condensed', sans-serif;
        }
    }
    h1 {
        color: var(--color-primary);
        font-size: 6rem;
    }
    h2 {
        font-size: 5rem;
        // letter-spacing: 2px;
        line-height: 35px;
    }
    h3 {
        font-size: 30px;
    }
    h4 {
        font-size: 40px;
    }
    h5 {
        font-size: 30px;
    }
    p {
        font-size: 18px;
        margin: 0;
    }
    @media screen and (min-width: 0px) {
        .button {
            border: none;
            font-family: 'Roboto Condensed', sans-serif;
            text-transform: uppercase;
            font-size: 18px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 50px;
            transition: var(--transition);
            text-decoration: none;
            cursor: pointer;
            &.button-primary {
                background-color: var(--color-primary);
                color: var(--color-white);
                &:hover {
                    background-color: var(--color-black);
                }
            }
            &.button-secondary {
                background-color: var(--color-black);
                color: var(--color-white);
                &:hover {
                    background-color: var(--color-primary);
                }
            }
        }
        .text-highlight {
            color: var(--color-primary);
        }
        .flex-column {
            display: flex;
            flex-direction: column;
        }
        .flex-row {
            display: flex;
            flex-direction: row;
            &.center-x {
                align-items: center;
            }
        }
        .gap-1 {
            gap: 1rem;
        }
        .gap-2 {
            gap: 2rem;
        }
        .gap-3 {
            gap: 3rem;
        }
        .gap-5 {
            gap: 5rem;
        }
        .gap-10 {
            gap: 10rem;
        }
        .section-header {
            text-align: center;
            h3 {
                color: var(--color-primary);
            }
        }
    }
    @media screen and (min-width: 768px) {
        h1 {
            font-size: 100px;
            line-height: 90px;
        }
        h2 {
            font-size: 80px;
            line-height: 65px;
        }
        .button {
            width: 200px;
        }
    }
</style>
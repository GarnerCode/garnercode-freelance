<template>
    <section id="testimonials">
        <div class="testimonial">
            <p class="quote">"Tyler is a team player and well-respected by his peers. He contributed positively to our work environment and displayed excellent problem-solving and communication skills."</p>
            <div class="credit">
                <img class="credit-img" src="https://media.licdn.com/dms/image/C5603AQGHzBb73A-t7g/profile-displayphoto-shrink_100_100/0/1547277520921?e=1687392000&v=beta&t=C5wBACKO8ZQa5K66z24ZMeF5ZoZY1i4LKbTrAk5Cb7A" alt="Rowan Kelly headshot">
                <p class="credit-text">Rowan Kelly, Director at Runway Proptech</p>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #testimonials {
            padding: 0 var(--mobile-x-padding);
            .testimonial {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                gap: 2rem;
                background-color: #fff;
                width: calc(100% - 4rem);
                padding: 20px;
                margin: 0 auto;
                
                .quote {
                    font-size: 18px;
                    font-style: italic;
                }
                .credit {
                    display: flex;
                    flex-direction: row;
                    gap: 1rem;
                    align-items: center;
                }
                .credit-img {
                    width: 60px;
                    border-radius: 100%;
                }
                .credit-text {
                    font-family: 'Roboto Condensed', sans-serif;
                    font-weight: bold;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #testimonials {
            padding: 0 var(--tablet-x-padding);
            position: relative;
            .testimonial {
                width: 400px;
                height: 180px;
                position: absolute;
                top: -110px;
                left: 0;
                right: 0;
                margin: 0 auto;
                box-shadow: var(--box-shadow);
                .credit {
                    gap: 2rem;
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #testimonials {
            .testimonial {
                width: 500px;
                height: 150px;
            }
        }
    }
</style>
<template>
    <section id="contact">
        <div class="section-header">
            <h3>Contact Me</h3>
            <h4>Let's Work Together</h4>
        </div>
        <div class="contact-container">
            <form>
                <input class="field" type="text" name="name" placeholder="Name">
                <input class="field" type="email" name="email" placeholder="Email">
                <input class="field" type="tel" name="phone" placeholder="Phone">
                <textarea class="field field-textarea" name="message" placeholder="Message"></textarea>
                <input type="submit" value="Submit" class="button button-primary">
            </form>
        </div>
    </section>
</template>

<style lang="scss">
    @media screen and (min-width: 0px) {
        #contact {
            padding: 0 var(--mobile-x-padding);
            .contact-container {
                display: flex;
                flex-direction: column;
                gap: 5rem;
                margin-top: 10rem;
            }
            form {
                display: flex;
                flex-direction: column;
                gap: 5rem;
            }
            .field {
                display: block;
                background: none;
                border: none;
                border-bottom: 1px solid var(--color-black);
                resize: none;
                font-size: 18px;
                padding: 1rem 2rem;
                transition: var(--transition);
                &.field-textarea {
                    height: 150px;
                }
                &:focus {
                    outline: none;
                    border-bottom: 1px solid var(--color-primary);
                }
                &.error {
                    border: 1px solid red;
                }
            }
        }
    }
    @media screen and (min-width: 768px) {
        #contact {
            padding: 0 var(--tablet-x-padding);
            form {
                width: 400px;
                margin: 0 auto;
                .button {
                    position: relative;
                    margin: 0 auto;
                }
            }
        }
    }
    @media screen and (min-width: 1440px) {
        #contact {
            padding: 0 var(--desktop-x-padding);
        }
    }
    @media screen and (min-width: 1920px) {
        #contact {
            padding: 0 var(--widescreen-x-padding);
        }
    }
</style>
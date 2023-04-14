<script>
export default {
    name: "AppFooter",
    data() {
        return {
        };
    },
}
</script>

<template>
    <section>
        <div class="container">
            <div class="container child">
                <div class="column">
                    <h2>About</h2>
                    <div class="line"></div>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi quibusdam rerum amet architecto,
                        aperiam enim at fuga!</p>
                    <div class="icons">
                        <i class="fa-brands fa-linkedin-in rounded"></i>
                        <i class="fa-brands fa-facebook-f square"></i>
                        <i class="fa-brands fa-twitter rounded"></i>
                    </div>
                </div>
                <div class="column">
                    <h2>Twitter</h2>
                    <div class="line"></div>
                    <div class="twitterBox"><i class="fa-brands fa-twitter"></i>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab nemo architecto tempora reiciendis
                            dolore nulla natus aspernatur</p>
                    </div>
                    <div class="twitterBox"><i class="fa-brands fa-twitter"></i>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab nemo architecto tempora reiciendis
                            dolore nulla natus aspernatur</p>
                    </div>
                </div>
                <div class="column">
                    <h2>Important Links</h2>
                    <div class="line"></div>
                    <ul>
                        <li><a href="">About me</a></li>
                        <li><a href="">About us</a></li>
                        <li><a href="">Language Packs</a></li>
                        <li><a href="">Become a coach</a></li>
                        <li><a href="">Monthly events</a></li>
                    </ul>
                </div>
                <div class="column">
                    <h2>Contact Me</h2>
                    <div class="line"></div>
                    <div class="contact"><i class="fa-solid fa-location-dot"></i><span> Via TaldeiTali, Speranza,
                            911</span></div>
                    <div class="contact"><i class="fa-solid fa-phone"></i><span> (+351) 333.179.3459</span></div>
                    <div class="contact"><i class="fa-regular fa-envelope"></i><span> everlead@studio.com</span></div>
                    <div class="footerform">
                        <label for="name"></label>
                        <input type="text" id="name" name="name" placeholder=" Your name" required>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;

section {
    background-color: $black-second-color;
    height: 400px;
    padding: 48px 0;
}

.container {
    @include mixins.container-margin;
    gap: 24px;
}

.child {
    @include mixins.d-flex-evenly;
}

.column {
    width: calc(100% / 4);
    height: 100%;
    align-self: flex-start;

    h2 {
        color: $white-first-color;
        font-size: 20px;
    }

    a,
    p,
    span {
        font-size: 14px;
        color: $gray-third-color;
        padding: 6px 0;
        display: inline-block;

        &:hover {
            color: $white-first-color;
        }
    }

    .line {
        margin: 8px 0;
        width: 60px;
        height: 1.5px;
        background-color: $orange-first-color;
    }
}

.icons {
    margin-top: 12px;

    i {
        cursor: pointer;
        margin-right: 8px;
        background-color: $white-first-color;
        border-radius: 50%;

        &:hover {
            background-color: $orange-first-color;
            color: $white-first-color;
        }
    }

    .square {
        padding: 3px 6px;
    }

    .rounded {
        padding: 3px;
    }
}

.twitterBox {
    display: flex;
    align-items: flex-start;

    i {
        padding: 8px;
        color: $orange-first-color;
    }
}

.contact {

    span {
        margin-left: 8px;
    }

    i {
        color: $orange-first-color;
    }
}

.footerform {
    margin-top: 8px;

    input {
        background-color: transparent;
        border: none;
        padding-bottom: 6px;
        border-bottom: 1px solid lightgray;
        width: 100%;
    }
}
</style>
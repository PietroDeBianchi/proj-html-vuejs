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
                        aperiam enim at quas, fuga, quaerat minus nihil iusto neque!</p>
                    <div class="icons">
                        <i class="fa-brands fa-linkedin"></i>
                        <i class="fa-brands fa-facebook"></i>
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                </div>
                <div class="column">
                    <h2>Twitter</h2>
                    <div class="line"></div>
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
                    <div><i class="fa-solid fa-location-dot"></i><span>Via TaldeiTali, Speranza, 911</span></div>
                    <div><i class="fa-solid fa-location-dot"></i><span>Via TaldeiTali, Speranza, 911</span></div>
                    <div><i class="fa-solid fa-location-dot"></i><span>Via TaldeiTali, Speranza, 911</span></div>
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
    p {
        font-size: 14px;
        color: $gray-third-color;
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
        margin-right: 8px;
        background-color: $white-first-color;
        padding: 3px;
        border-radius: 50%;
    }
}
</style>
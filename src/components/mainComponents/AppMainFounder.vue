<script>
export default {
    name: 'AppMainFounder',
    data() {
        return {
        }
    },
}

</script>

<template>
    <section>
        <div class="container">
            <div class="container">
                <img src="../../assets/img/h1-blog-img-04.jpg" alt="Founder">
                <div class="arrows">
                    <img class="reverse" src="../../assets/svg/svg-6.svg" alt="arrow">
                    <img src="../../assets/svg/svg-6.svg" alt="arrow">
                </div>
                <img src="../../assets/svg/svg-4.svg" alt="background" class="background">
                <div class="founderCard">
                    <h2>Max Power</h2>
                    <span>Founder and Executive Director</span>
                    <div class="line"></div>
                    <p>Max Power, he's the man whose name you'd love to touch but you mustn't touch, his name sounds good
                        in your ear but when you say it, you mustn't fear!</p>
                    <div class="icons">
                        <i class="fa-brands fa-linkedin"></i>
                        <i class="fa-brands fa-facebook"></i>
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

section {
    height: 500px;
    min-width: 1200px;
    background-color: $gray-first-color;
}

.container {
    @include mixins.container-margin;
    position: relative;

    img {
        width: 500px;
    }

    .arrows {
        font-size: 0;
        position: absolute;
        background-color: $orange-first-color;
        padding: 16px 20px;
        bottom: 5px;

        .reverse {
            transform: scaleX(-1);
            margin-right: 8px;
        }

        img {
            width: 20px;
        }
    }
}

.founderCard {

    background-color: $white-first-color;
    position: absolute;
    top: 50%;
    left: 75%;
    transform: translate(-50%, -50%);
    width: 50%;
    padding: 32px;

    .line {
        margin: 8px 0;
        width: 80px;
        height: 1.5px;
        background-color: $orange-first-color;
    }

    .icons {
        margin-top: 12px;

        i {
            font-size: 24px;
            padding-right: 8px;
            cursor: pointer;

            &:hover {
                color: $orange-first-color;
            }
        }
    }
}

.background {
    position: absolute;
    width: 360px;
    left: 71%;
    top: -29%;
    opacity: 0.7;
}
</style>
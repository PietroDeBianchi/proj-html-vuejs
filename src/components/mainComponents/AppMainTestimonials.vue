<script>
export default {
    name: 'AppMainTestimonials',
    data() {
        return {
        }
    },
}

</script>

<template>
    <section>
        <div class="container">
            <img class="arrow front" src="../../assets/svg/svg-6.svg" alt="arrow">
            <img class="arrow back" src="../../assets/svg/svg-6.svg" alt="arrow">
            <div class="container parent">
                <h2>Testimonials.</h2>
                <div class="testimonialBox">
                    <img src="../../assets/img/h3-img-04.png" alt="testimonial">
                    <h4>Niko Robin</h4>
                    <p>"Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia ipsam itaque corporis quidem
                        deserunt quis in magni."</p>
                    <div class="testimonialSelect">
                        <span>01</span>
                        <div class="line">
                            <div class="scroll"></div>
                        </div>
                        <span>03</span>
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
    background-color: $black-second-color;
    height: 400px;
}

.container {
    @include mixins.container-margin;
    text-align: center;
    height: 100%;
    position: relative;

    h2 {
        font-size: 150px;
        line-height: 120px;
        opacity: 0.4;
    }

    .arrow {
        position: absolute;
        top: 50%;
    }

    .front {
        left: 100%;
    }

    .back {
        right: 100%;
        transform: scaleX(-1);
    }
}

.testimonialBox {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    img {
        border: 1px solid lightgrey;
        border-radius: 50%;
    }

    h4 {
        color: $white-first-color;
        margin: 12px 0;
    }

    p {
        color: $gray-second-color;
    }
}

.testimonialSelect {
    width: 60%;
    margin: auto;
    @include mixins.d-flex-evenly;
    padding: 24px 0;

    span {
        color: $gray-second-color;
        font-size: 8px;
    }

    .line {
        position: relative;
        width: 70%;
        height: 2px;
        background-color: $black-third-color;
        margin: 0 6px;

        .scroll {
            position: absolute;
            background-color: $gray-second-color;
            width: calc(100% / 3);
            height: 2px;
        }
    }
}
</style>
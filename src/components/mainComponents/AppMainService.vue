<script>
export default {
    name: 'AppMainService',
    data() {
        return {
            services: [
                {
                    image: "/src/assets/svg/svg-0.svg",
                    title: "Knowing",
                    text: "In-depth knowledge of business needs and available facilities",
                },
                {
                    image: "/src/assets/svg/svg-1.svg",
                    title: "Selling",
                    text: "We have a team of experts available to expand your sales network",
                },
                {
                    image: "/src/assets/svg/svg-2.svg",
                    title: "Learning",
                    text: "Our support service also enables in-house training for the company",
                },
                {
                    image: "/src/assets/svg/svg-3.svg",
                    title: "Contantct",
                    text: "We offer an extensive network of contacts to facilitate your needs",
                },
            ]
        };
    },
}
</script>

<template>
    <section>
        <div class="serviceList">
            <div class="serviceText">
                <h2>Our Specialities<span>.</span></h2>
                <p>We offer a wide range of services</p>
            </div>
            <div class="container">
                <div class="serviceCard" v-for="service in services" :key="index">
                    <img :src="service.image" :alt="service.title">
                    <h3>{{ service.title }}</h3>
                    <p>{{ service.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

span {
    color: $orange-first-color;
}

section {
    position: relative;
    height: 500px;
    background-color: $gray-first-color;
}

.serviceList {
    @include mixins.container-margin;
    background-color: $white-first-color;
    text-align: center;
    padding: 24px;
    position: absolute;
    left: 50%;
    top: 30%;
    transform: translate(-50%, -50%);

    .serviceText {
        h2 {
            font-size: 32px;
            margin-bottom: 12px;
        }

        p {
            margin-bottom: 12px;
        }
    }

    .container {
        @include mixins.container-margin;
        @include mixins.d-flex-between;
        gap: 20px;
        padding-bottom: 12px;

        img {
            min-height: 160px;
            min-width: 160px;
            margin-bottom: 12px;
        }

        p {
            font-size: 15px;
            margin-top: 12px;
        }
    }
}
</style>
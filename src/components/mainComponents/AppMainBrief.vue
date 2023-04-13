<script>
export default {
    name: 'AppMainBrief',
    data() {
        return {
            skills: [
                {
                    service: "Mentorship",
                    percentage: "78%",
                },
                {
                    service: "Education",
                    percentage: "95%",
                }, {
                    service: "Learning",
                    percentage: "65%",
                }, {
                    service: "Motivation",
                    percentage: "83%",
                },
            ]
        }
    },
}

</script>

<template>
    <section>
        <div class="container">
            <div class="container child">
                <div class="descriptionBox">
                    <h2>Creative Leader<span>.</span></h2>
                    <div class="line"></div>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur asperiores similique culpa
                        dolores? Eveniet magni obcaecati enim temporibus rem facilis omnis vitae nisi quasi, maxime voluptas
                        corrupti velit perspiciatis beatae.</p>
                    <h5>READ MORE</h5>
                </div>
                <div class="skillsBox">
                    <div class="skill" v-for="(skill, index) in skills" :key="index">
                        <div class="skillStats">
                            <span>{{ skill.service }}</span><span>{{ skill.percentage }}</span>
                        </div>
                        <div class="skillPercentage">
                            <div class="percentageLine" :style="{ width: parseInt(skill.percentage) + '%' }"></div>
                        </div>
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
    padding: 96px 0;
}

.container {
    @include mixins.container-margin;

    .child {
        display: flex;
    }

    .descriptionBox,
    .skillsBox {
        width: 50%;
    }
}

.descriptionBox {

    p {
        margin-bottom: 12px;
        color: $gray-third-color;
    }

    span {
        color: $orange-first-color;
    }

    .line {
        margin: 8px 0;
        width: 80px;
        height: 1.5px;
        background-color: $orange-first-color;
    }
}

.skillsBox {

    .skill {
        height: calc(100% /4);
    }

    .skillStats {
        @include mixins.d-flex-between;
        margin-bottom: 6px;
    }

    .skillPercentage {
        width: 100%;
        height: 3px;
        position: relative;
        background-color: $gray-second-color;

        .percentageLine {
            position: absolute;
            height: 3px;
            background-color: $orange-first-color;
        }
    }
}
</style>
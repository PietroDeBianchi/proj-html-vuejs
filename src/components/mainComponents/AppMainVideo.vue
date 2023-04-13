<script>
export default {
    name: 'AppMainVideo',
    data() {
        return {
        }
    },
}

</script>

<template>
    <section>
        <i class="fa-solid fa-play"></i>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

section {
    background-image: url(../../assets/img/h1-img-04.jpg);
    background-size: cover;
    height: 600px;
    position: relative;

    i {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 40px;
        color: $white-second-color;
        padding: 15px 20px;
        border-radius: 50%;

        &:hover {
            cursor: pointer;
            background-color: $gray-third-color;
        }

    }
}
</style>
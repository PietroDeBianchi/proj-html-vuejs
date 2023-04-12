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
            <div class="container">
                <h1>TESTIMONIALS</h1>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

.container {
    @include mixins.container-margin;
}
</style>
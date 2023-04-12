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
        <div class="container">
            <div class="container">
                <h1>VIDEO</h1>
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
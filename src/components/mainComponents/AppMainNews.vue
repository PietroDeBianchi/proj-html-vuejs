<script>
export default {
    name: 'AppMainNews',
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
                <div class="titleBox">
                    <h2>Latest News<span>.</span></h2>
                    <p>Stay up to date on the latest news and events from of Everlead</p>
                    <div class="line"></div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../../styles/partials/mixins";
@use "../../styles/partials/variables" as *;

section {
    background-color: $gray-first-color;
    padding: 24px;
}

.container {
    @include mixins.container-margin;
}

.titleBox {
    width: 100%;
    text-align: center;

    h2 {
        font-size: 40px;
    }

    span {
        color: $orange-first-color;
    }

    p {
        margin-bottom: 12px;
    }

    .line {
        margin: auto;
        width: 80px;
        height: 1.5px;
        background-color: $orange-first-color;
    }
}
</style>
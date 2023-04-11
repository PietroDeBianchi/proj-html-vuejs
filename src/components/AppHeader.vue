<script>
export default {
    name: "AppHeader",
    data() {
        return {
            navbar: ["HOMES", "PAGES", "BLOG", "SHOP", "EVENTS", "ELEMENTS"]
        };
    },
}
</script>

<template>
    <section id="navigator">
        <div class="container">
            <h2>Everlead<span>.</span></h2>
            <nav>
                <ul class="headerNavbar">
                    <li v-for="(element) in navbar">
                        <a class="nav-element" href="#"> {{ element }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </section>
    <section id="jumbo">
        <div class="container">
            <div class="text-box">
                <h1>Our Teams<span>.</span></h1>
                <p>We helps realties to develop their business, our professional team will help
                    you to align your business strategy to the market trends and opportunities.</p>
            </div>

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;

// general tags
span {
    color: $orange-first-color;
}

//top header-navigator style
#navigator {
    position: fixed;
    width: 100vw;
    padding: 12px 0;

    .container {
        @include mixins.d-flex-between;
        width: 90%;
        margin: auto;

        h2 {
            font-size: 32px;
        }
    }

    .headerNavbar {
        @include mixins.d-flex-between;
        gap: 2rem;
    }
}

//top header-Jumbo style
#jumbo {
    background-image: url(../assets/img/rev-slider-main-home-img-03.jpg);
    background-size: cover;
    height: 600px;

    .container {
        @include mixins.container-margin;
        position: relative;
    }

    .text-box {
        position: absolute;
        top: 320px;
        width: 30%;

        h1 {
            font-size: 42px;
        }
    }

}
</style>
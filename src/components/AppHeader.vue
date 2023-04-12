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
                <div class="btn-box">
                    <button class="read-btn">READ MORE<i class="fa-solid fa-arrow-right-long"></i></button>
                    <button class="purchase-btn">PURCHASE<i class="fa-solid fa-arrow-right-long"></i></button>
                </div>
            </div>

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;

// GENERAL TAGS
span {
    color: $orange-first-color;
}

//HEADER-NAVIGATOR STYLE
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

        a {
            color: $black-third-color;

            &:hover {
                color: $orange-first-color;
            }
        }
    }
}

//HEADER-JUMBO STYLE
#jumbo {
    background-image: url(../assets/img/rev-slider-main-home-img-03.jpg);
    background-size: cover;
    height: 600px;
    text-align: start;

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
            margin-bottom: 24px;
        }
    }

    // HEADER-JUMBO-BUTTON STYLE
    .btn-box {
        display: flex;
        margin-top: 24px;
        gap: 16px;

        .read-btn {
            @include mixins.button-white;
            background-color: $white-first-color;
        }

        .purchase-btn {
            @include mixins.button-orange;
            background-color: $orange-first-color;
        }
    }
}
</style>
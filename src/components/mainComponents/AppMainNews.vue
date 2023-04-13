<script>
export default {
    name: 'AppMainNews',
    data() {
        return {
            news: [
                {
                    image: "/src/assets/img/h1-blog-img-01.jpg",
                    date: "May 15, 2019",
                    writer: "David Linch",
                    title: "Next Investiments",
                    text: "In this article we will talk about...",
                },
                {
                    image: "/src/assets/img/h1-blog-img-02.jpg",
                    date: "December 5, 2021",
                    writer: "Peter Jackson",
                    title: "Team Building",
                    text: "In this article we will talk about...",
                },
                {
                    image: "/src/assets/img/h1-blog-img-03.jpg",
                    date: "March 29, 2023",
                    writer: "Quentin Tarantino",
                    title: "New Business Day",
                    text: "In this article we will talk about...",
                }
            ]
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
                <div class="newsList">
                    <div class="newsBox" v-for="(article, index) in news" :key="index">
                        <img :src="article.image" :alt="article.title">
                        <span><i class="fa-regular fa-clock"></i> {{ article.date }}</span><span><i
                                class="fa-regular fa-user"></i>{{ article.writer }}</span>
                        <h3>{{ article.title }}</h3>
                        <p>{{ article.text }}</p>
                        <h5> READ MORE </h5>
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
    background-color: $gray-first-color;
    padding: 32px 0;
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

.newsList {
    @include mixins.d-flex-between;
    margin-top: 24px;

    .newsBox {
        width: calc(100% / 3 - 16px);

        img {
            width: 100%;
            margin-bottom: 12px;
        }

        span {
            font-size: 12px;
            padding-right: 8px;
            color: $gray-third-color;
        }

        i {
            padding-right: 4px;
            color: $orange-first-color;
        }

        h3 {
            font-size: 24px;
            padding: 4px 0;
        }

        p {
            font-size: 14px;
            color: $gray-third-color;
            margin-bottom: 12px;
        }

        h5:hover {
            color: $orange-first-color;
            cursor: pointer;
        }
    }
}
</style>
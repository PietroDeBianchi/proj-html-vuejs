<script>
export default {
    name: 'AppMainEvents',
    data() {
        return {
            events: [
                {
                    location: "Melbourne Coaching",
                    date: "07 Jan 2022",
                    hour: "9:00 am - 5:00 pm",
                    location: "Pier St, Port Melbourne VIC 3207, Australia",
                },
                {
                    location: "New York Coaching",
                    date: "23 Jan 2022",
                    hour: "9:00 am - 5:00 pm",
                    location: "Lincoln C. Plaza, New York, NY 10023, Stati Uniti",
                }, {
                    location: "London Coaching",
                    date: "09 Feb 2022",
                    hour: "9:00 am - 5:00 pm",
                    location: "County Hall, London SE1 7PB, Regno Unito",
                }, {
                    location: "Rome Coaching",
                    date: "15 Feb 2022",
                    hour: "9:00 am - 5:00 pm",
                    location: "Piazza di Trevi, 00187 Roma RM",
                },
            ]
        }
    },
}

</script>

<template>
    <section>
        <div class="container">
            <div class="container">
                <div class="eventsList">
                    <h2>Upcoming Events</h2>
                    <div class="event" v-for="event in events" :key="index">
                        <h4>{{ event.location }}</h4>
                        <span>{{ event.hour }}, {{ event.date }}</span>
                        <p>{{ event.location }}</p>
                        <h5>READ MORE</h5>
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
    height: 700px;
    background-image: url(../../assets/img/h1-img-09.jpg);
    background-size: cover;

    .container {
        @include mixins.container-margin;
        position: relative;
        height: 100%;
    }
}

.eventsList {
    background-color: $white-first-color;
    width: 50%;
    position: absolute;
    top: 50%;
    left: 25%;
    transform: translate(-50%, -50%);

    h2 {
        padding: 12px;
        background-color: $gray-first-color;
    }
}

.event {
    padding: 12px;
    border-bottom: 1px solid lightgrey;

    &:hover {
        background-color: $gray-first-color;
    }

    h4,
    p,
    span {
        padding: 6px 0;
    }

    p,
    span {
        color: $black-first-color;
        font-size: 12px;
    }

    h4 {
        font-size: 16px;
    }
}
</style>
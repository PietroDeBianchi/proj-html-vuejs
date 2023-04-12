<script>
export default {
    name: 'AppMainEvents',
    data() {
        return {
            events: [
                {
                    city: "Melbourne Coaching",
                    hour: "9:00 am - 5:00 pm",
                    location: "Pier St, Port Melbourne VIC 3207, Australia",
                    date: [
                        {
                            day: "07",
                            month: "Jan ",
                            year: "2022"
                        }
                    ]
                },
                {
                    city: "New York Coaching",
                    hour: "9:00 am - 5:00 pm",
                    location: "Lincoln C. Plaza, New York, NY 10023, Stati Uniti",
                    date: [
                        {
                            day: "23",
                            month: "Jan ",
                            year: "2022"
                        }
                    ]
                },
                {
                    city: "London Coaching",
                    hour: "9:00 am - 5:00 pm",
                    location: "County Hall, London SE1 7PB, Regno Unito",
                    date: [
                        {
                            day: "09",
                            month: "Feb ",
                            year: "2022"
                        }
                    ]
                },
                {
                    city: "Rome Coaching",
                    hour: "9:00 am - 5:00 pm",
                    location: "Piazza di Trevi, 00187 Roma RM",
                    date: [
                        {
                            day: "27",
                            month: "Feb ",
                            year: "2022"
                        }
                    ]
                },
            ]
        }
    }
}

</script>

<template>
    <section>
        <div class="container">
            <div class="container">
                <div class="eventsList">
                    <h2>Upcoming Events</h2>
                    <div class="event" v-for="(event, index) in events" :key="index">
                        <div class="dateBox">
                            <h4>{{ event.date[0].day }}</h4>
                            <h6>{{ event.date[0].month }}{{ event.date[0].year }}</h6>
                        </div>
                        <div>
                            <h4>{{ event.city }}</h4>
                            <span>{{ event.hour }}, {{ event.date[0].day }} {{ event.date[0].month }} {{ event.date[0].year
                            }}</span>
                            <p>{{ event.location }}</p>
                            <h5>READ MORE</h5>
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
    width: 45%;
    position: absolute;
    top: 50%;
    left: 25%;
    transform: translate(-50%, -50%);

    h2 {
        padding: 12px 24px;
        background-color: $gray-first-color;
    }
}

.event {
    padding: 12px 24px;
    border-bottom: 1px solid lightgrey;

    &:hover {
        background-color: $gray-first-color;
    }

    div {
        display: inline-block;
    }

    p,
    span {
        padding-bottom: 8px;
    }

    p,
    span,
    h5 {
        color: $black-first-color;
        font-size: 12px;
    }

    h4 {
        font-size: 16px;
    }

    .dateBox {
        background-color: $orange-first-color;
        color: $white-first-color ;
        margin-right: 24px;
        padding: 8px;
        text-align: center;
        vertical-align: top;
    }
}
</style>
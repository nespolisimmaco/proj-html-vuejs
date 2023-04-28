<script>
export default {
    name: "UpcomingEvents",
    data() {
        return {
            events: [
                {
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
                },
                {
                    place: "New york, US",
                    title: "Painting Art Contest 2020",
                    day: "10",
                    month: "OCT"
                },
                {
                    place: "Hamburg, Germany",
                    title: "International Art Fair 2020",
                    day: "23",
                    month: "NOV"
                },
                {
                    place: "Illinois, US",
                    title: "Street Performance: Call for Artist",
                    day: "15",
                    month: "DEC"
                },
                {
                    place: "Illinois, US",
                    title: "Consumer Food Safety Education Conference",
                    day: "22",
                    month: "JUL"
                },
                {
                    place: "Dubai",
                    title: "How meditation improves your mental health?",
                    day: "12",
                    month: "AUG"
                },
            ]
        }
    }
}
</script>
        
<template>
    <!-- Upcoming events -->
    <div class="upcoming-events text-center">
        <!-- Container -->
        <div class="ms_container">
            <!-- Container fluid -->
            <div class="container-fluid">
                <h5>Wanna transform your life?</h5>
                <h2>Upcoming Events</h2>
                <!-- Row -->
                <div class="row row-cols-2 g-4 mt-4 mb-5">
                    <!-- Column -->
                    <div class="col" v-for="(event, index) in events" :key="index">
                        <!-- Card -->
                        <div class="ms_card py-3 px-4">
                            <!-- Inner row -->
                            <div class="row">
                                <!-- Inner column -->
                                <div class="col-8 text-start">
                                    <div class="place my-2">{{ event.place }}</div>
                                    <div class="title">{{ event.title }}</div>
                                </div>
                                <!-- Inner column -->
                                <div class="col-4">
                                    <div class="day">{{ event.day }}</div>
                                    <div class="month">{{ event.month }}</div>
                                    <button class="btn">Get ticket</button>
                                </div>
                            </div>
                            <!-- End Inner row -->
                        </div>
                        <!-- End Card -->
                    </div>
                    <!-- End Column -->
                </div>
                <!-- End Row -->
                <div class="view-events">
                    Excited about our event? <a href="#">View all events &rarr;</a>
                </div>
            </div>
            <!-- End Container fluid -->
        </div>
        <!-- End Container -->
    </div>
    <!-- End Upcoming events -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.ms_container {
    @include ms_container();
}

.upcoming-events {
    padding: 4rem 0;

    h5 {
        color: $main-green;
    }

    h2 {
        font-weight: 700;
        margin-top: 1rem;
    }
}

.ms_card {
    background-color: $jumbotron-background;
    border-radius: 5px;
    transition: all 0.2s;

    &:hover {
        border-left: 5px solid $main-green;

        button {
            background-color: $hover-button;
        }
    }

    .place {
        font-size: .7rem;
        color: grey;

        &::before {
            content: '\f3c5';
            font-family: FontAwesome;
            font-weight: normal;
            font-style: normal;
            margin-right: 5px;
        }
    }

    .title {
        font-weight: 600;
    }

    .day {
        color: $main-green;
        font-size: 2.5rem;
    }

    .month {
        font-weight: 600;
        margin-bottom: 5px;
    }

    button {
        background-color: $main-green;
        color: white;
        font-size: .8rem;
        font-weight: 700;
        padding: 5px 1.8rem;
    }
}

.view-events {
    font-size: .8rem;
    font-weight: 500;

    a {
        color: $main-green;
        font-weight: 700;
        text-decoration-color: lightgrey;
    }
}
</style>
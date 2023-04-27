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
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
                },
                {
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
                },
                {
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
                },
                {
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
                },
                {
                    place: "Texas, US",
                    title: "Storytelling Workshop",
                    day: "22",
                    month: "NOV"
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
                <div class="row row-cols-2 g-4 mt-4">
                    <div class="col" v-for="(event, index) in events" :key="index">
                        <div class="ms_card">
                            <div class="place">{{ event.place }}</div>
                            <div class="title">{{ event.title }}</div>
                            <div class="day">{{ event.day }}</div>
                            <div class="month">{{ event.month }}</div>
                            <button class="btn">Get ticket</button>
                        </div>
                    </div>
                </div>
                <!-- End Row -->
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
}
</style>
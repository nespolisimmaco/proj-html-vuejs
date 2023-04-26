<script>
export default {
    name: "CompanyFeatures",
    data() {
        return {
            features: [
                {
                    title: "One to One",
                    description: "Getting the necessary clarity about the current state to help ypu improve your game."
                },
                {
                    title: "Anywhere",
                    description: "Access to valuable and portable program which allow you to setup and live anywhere you want."
                },
                {
                    title: "On Time",
                    description: "Punctuality is our top priority because it's an essential criteria to assess a program quality."
                },
                {
                    title: "Online Courses",
                    description: "Online business coaching now offers you a very powerful way to empower your business into success."
                },
                {
                    title: "Consulting",
                    description: "You will get a clear sense of direction for your business, thorough assessment and faster results."
                },
                {
                    title: "Self Development",
                    description: "Business Coaching often kep your focus and develop you both in a professional and personal way."
                },
            ]
        }
    }
}
</script>

<template>
    <!-- Features -->
    <div class="features text-center">
        <!-- Container -->
        <div class="ms_container">
            <h5>Let's Dream Big Together</h5>
            <h2>We are pioneers of the digital approach, using leading-edge technology to simplify procedures and apply
                executive coaching in the new age of digitalization.</h2>
            <!-- Container fluid -->
            <div class="container-fluid">
                <!-- Row -->
                <div class="row row-cols-3 g-5">
                    <!-- Column -->
                    <div class="col text-start" v-for="(feature, index) in features" :key="index">
                        <h4>{{ feature.title }}</h4>
                        <p>{{ feature.description }}</p>
                    </div>
                    <!-- End Column -->
                </div>
                <!-- End Row -->
            </div>
            <!-- End Container fluid -->
            <div class="buttons mt-5">
                <button class="btn white-button">Learn more</button>
                <button class="btn green-button">Get started today</button>
            </div>
        </div>
        <!-- End Container -->
    </div>
    <!-- End Features -->
</template>


<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.features {
    padding: 5rem 0 4rem;
}

.ms_container {
    @include ms_container();

    h5 {
        color: $main-green;
    }

    h2 {
        margin: 2rem 0 3rem;
    }
}

.col {
    p {
        font-size: .9rem;
    }
}

.white-button {
    color: $main-green;
    font-weight: 600;
    font-size: .8rem;
    border: 1px solid lightgrey;
    padding: 10px 2rem;
    margin-right: 10px;
}

.green-button {
    background-color: $main-green;
    font-weight: 600;
    font-size: .8rem;
    padding: 10px 2rem;
    color: white;
    margin-left: 10px;
}
</style>
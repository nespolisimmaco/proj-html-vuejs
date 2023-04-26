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
                    title: "One to One",
                    description: ""
                },
                {
                    title: "One to One",
                    description: "Getting the necessary clarity about the current state to help ypu improve your game"
                },
                {
                    title: "One to One",
                    description: "Getting the necessary clarity about the current state to help ypu improve your game"
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
            <div class="container-fluid">
                <div class="row row-cols-3">

                </div>
            </div>
        </div>
        <!-- End Container -->
    </div>
    <!-- End Features -->
</template>


<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.ms_container {
    @include ms_container();
}
</style>
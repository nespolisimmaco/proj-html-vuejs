<script>
export default {
    name: "CompanyServices",
    data() {
        return {
            services: [
                {
                    title: "Consultative Training",
                    paragraph: "Lorem ipsum"
                },
                {
                    title: "Real Deal Coaching",
                    paragraph: "Lorem ipsum"
                },
                {
                    title: "Advisor Training Program",
                    paragraph: "Lorem ipsum"
                },
            ]
        }
    }
}
</script>
        
<template>
    <!-- Services -->
    <div class="services text-center">
        <!-- Container -->
        <div class="ms_container">
            <!-- Container fluid -->
            <div class="container-fluid">
                <h5>Let's Dream Big Together</h5>
                <h2>Explore How can I help you</h2>
                <!-- Row -->
                <div class="row row-cols-3">

                </div>
                <!-- Row -->
            </div>
            <!-- Container fluid -->
        </div>
        <!-- Container -->
    </div>
    <!-- Services -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.ms_container {
    @include ms_container();
}

.services {
    background-color: $jumbotron-background;

    h5 {
        color: $main-green;
    }

    h2 {
        font-weight: 600
    }
}

.card-footer {
    a {
        text-decoration: none;
        color: $main-green;
    }
}
</style>
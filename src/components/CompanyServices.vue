<script>
export default {
    name: "CompanyServices",
    data() {
        return {
            services: [
                {
                    image: "home-business-service-slide-01-480x298.jpg",
                    title: "Consultative Training",
                    paragraph: "With a coach adrressing multiple issues that are off balance, affecting your business in various unconsidered ways."
                },
                {
                    image: "home-business-service-slide-02-480x298.jpg",
                    title: "Real Deal Coaching",
                    paragraph: "Brings an exceptionally powerful opportunity. Being able to accept, to work with that oppurtunity."
                },
                {
                    image: "home-business-service-slide-03-480x298.jpg",
                    title: "Advisor Training Program",
                    paragraph: "Getting high quality, entrepreneur mindset driven online business coaching, is what is needed."
                },
            ]
        }
    },
    methods: {
        getImagePath(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
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
                <div class="row row-cols-3 mt-5">
                    <!-- Column -->
                    <div class="col" v-for="(service, index) in services">
                        <!-- Card -->
                        <div class="card h-100">
                            <img :src="getImagePath(service.image)" class="card-img-top" alt="...">
                            <div class="card-body">
                                <h5 class="card-title">{{ service.title }}</h5>
                                <p class="card-text">{{ service.paragraph }}</p>
                            </div>
                            <div class="card-footer">
                                <a href="#">Discover now &rarr;</a>
                            </div>
                        </div>
                        <!-- End Card -->
                    </div>
                    <!-- Column -->
                </div>
                <!-- Row -->
            </div>
            <!-- Container fluid -->
            <div class="dots d-flex justify-content-center align-items-center mt-4">
                <div class="dot active mx-2"></div>
                <div class="dot mx-2"></div>
                <div class="dot mx-2"></div>
            </div>
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
    padding: 4rem 0;

    h5 {
        color: $main-green;
    }

    h2 {
        font-weight: 600;
        margin: 1rem 0;
    }
}

.card {
    box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
}

.card-body {
    h5 {
        color: black;
    }

    p {
        font-size: .8rem;
    }
}

.card-footer {
    background-color: white;
    transition: all 0.3s;

    a {
        text-decoration: none;
        color: $main-green;
        font-size: .8rem;
        font-weight: 700;
    }

    &:hover {
        background-color: $main-green;

        a {
            color: white;
        }
    }
}

.dot {
    width: 7px;
    height: 7px;
    background-color: lightgrey;
    border-radius: 50%;

    &.active {
        width: 10px;
        height: 10px;
        background-color: black;
    }
}
</style>
<script>
export default {
    data() {
        return {
            courses: [
                {
                    image: "course-02-443x600.jpg",
                    price: "$40.00",
                    title: "Learning to Write as a Professional Author",
                },
                {
                    image: "stock-full-hd-03-443x600.jpg",
                    price: "Free",
                    title: "Customer-centric Info-Tech Strategies",
                },
                {
                    image: "stock-full-hd-04-443x600.jpg",
                    price: "$19.00",
                    title: "Open Programming Courses for Everyone: Python",
                },
                {
                    image: "stock-full-hd-06-443x600.jpg",
                    price: "$26.00",
                    title: "Academic Listening and Note-taking",
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
    <div class="courses text-center">
        <!-- Container -->
        <div class="container">
            <h5>Let's Dream Big Together</h5>
            <h2>Explore How can I help you</h2>
            <!-- Row -->
            <div class="row row-cols-4">
                <!-- Column -->
                <div class="col text-start" v-for="(course, index) in courses" :key="index">
                    <!-- Card -->
                    <div class="card">
                        <img :src="getImagePath(course.image)" class="card-img" alt="Course">
                        <div class="card-img-overlay d-flex flex-column justify-content-end">
                            <h5 class="card-title">{{ course.price }}</h5>
                            <p class="card-text">{{ course.title }}</p>
                        </div>
                    </div>
                    <!-- Card -->
                </div>
                <!-- End Column -->
            </div>
            <!-- End Row -->
        </div>
        <!-- End Container -->
    </div>
</template>


<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.courses {
    padding: 6rem 0;

    h5 {
        color: $main-green;
    }

    h2 {
        font-weight: 600;
        margin: 1rem 0 3rem;
    }
}

.card-img-overlay {
    background: linear-gradient(to top, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 0.4) 20%, rgba(0, 0, 0, 0) 100%);

    .card-title {
        font-weight: 700;
    }

    .card-text {
        color: white;
        font-weight: 700;
    }
}
</style>
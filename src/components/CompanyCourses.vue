<script>
export default {
    data() {
        return {
            courses: [
                {
                    image: "course-02-443x600.jpg",
                    price: "$40.00",
                    title: "Learning to Write as a Professional Author",
                    lessons: "20 Lessons",
                    students: "50 Students",
                    description: "The purpose of this course is to provide the advanced writing techniques commonly used for inspiring readers and ..."
                },
                {
                    image: "stock-full-hd-03-443x600.jpg",
                    price: "Free",
                    title: "Customer-centric Info-Tech Strategies",
                    lessons: "20 Lessons",
                    students: "50 Students",
                    description: "The purpose of this course is to provide the advanced writing techniques commonly used for inspiring readers and ..."
                },
                {
                    image: "stock-full-hd-04-443x600.jpg",
                    price: "$19.00",
                    title: "Open Programming Courses for Everyone: Python",
                    lessons: "20 Lessons",
                    students: "50 Students",
                    description: "The purpose of this course is to provide the advanced writing techniques commonly used for inspiring readers and ..."
                },
                {
                    image: "stock-full-hd-06-443x600.jpg",
                    price: "$26.00",
                    title: "Academic Listening and Note-taking",
                    lessons: "20 Lessons",
                    students: "50 Students",
                    description: "The purpose of this course is to provide the advanced writing techniques commonly used for inspiring readers and ..."
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
                            <div class="course">
                                <div class="d-flex justify-content-start">
                                    <div class="lessons me-4">{{ course.lessons }}</div>
                                    <div class="students">{{ course.students }}</div>
                                </div>
                                <p class="description">{{ course.description }}</p>
                            </div>
                        </div>
                    </div>
                    <!-- Card -->
                </div>
                <!-- End Column -->
            </div>
            <!-- End Row -->
            <!-- Call to action -->
            <div class="cta mt-5">
                <p>Take the control of their life back and start doing things to make their dreams come true. <a
                        href="#">View
                        all courses &rarr;</a></p>
            </div>
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

// Card
.card {
    .card-img-overlay {
        background: linear-gradient(to top, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 0.4) 20%, rgba(0, 0, 0, 0) 100%);

        .card-title {
            font-weight: 700;
        }

        .card-text {
            color: white;
            font-weight: 700;
        }

        .lessons,
        .students,
        .description {
            color: white;
            font-size: .8rem;
            font-weight: 500;
            opacity: 0;
            visibility: hidden;
            max-height: 0;
            transition: all 0.3s;
        }

        &:hover {

            .lessons,
            .students,
            .description {
                opacity: 1;
                visibility: visible;
                max-height: 100px;
            }
        }
    }
}

// Call to action
.cta {
    width: 40%;
    margin: 0 auto;

    a {
        color: black;
        text-decoration: underline lightgrey;
        font-weight: 600;
    }
}
</style>
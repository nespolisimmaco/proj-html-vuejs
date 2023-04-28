<script>
export default {
    name: "Reviews",
    data() {
        return {
            reviews: [
                {
                    title: "It's a choice of quality for people with special needs",
                    paragraph: "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine, MaxCoach guys just got me.",
                    photo: "testimonial-avata-03.jpg",
                    name: "FLORENCE THEMES",
                    work: "/Multimedia Admin"
                },
                {
                    title: "High level of efficiency and scientific teaching methods",
                    paragraph: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                    photo: "testimonial-avata-02.jpg",
                    name: "MINA HOLLACE",
                    work: "/Freelancer"
                },
                {
                    title: "Professional team of specialists and passionate mentors at reach",
                    paragraph: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
                    photo: "testimonial-avata-04.jpg",
                    name: "MADLEY PONDOR",
                    work: "/IT Specialist"
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
    <!-- Reviews -->
    <div class="reviews text-center">
        <!-- Container fluid -->
        <div class="container-fluid">
            <h5>People are praising MaxCoach</h5>
            <h2>What make they love us?</h2>
            <!-- Row -->
            <div class="row row-cols-3 mt-5">
                <!-- Column -->
                <div class="col" v-for="(review, index) in reviews" :key="index">
                    <!-- Card -->
                    <div class="ms_card rounded text-start h-100" :class="index == 0 || index == 2 ? 'opaque' : ''">
                        <h6>{{ review.title }}</h6>
                        <p>{{ review.paragraph }}</p>
                        <!-- User -->
                        <div class="user d-flex justify-content-start align-items-center">
                            <img :src="getImagePath(review.photo)" alt="User">
                            <div>
                                <div class="name">{{ review.name }}</div>
                                <div class="work">{{ review.work }}</div>
                            </div>
                        </div>
                        <!-- End User -->
                    </div>
                    <!-- End Card -->
                </div>
                <!--End  Column -->
            </div>
            <!-- End Row -->
        </div>
        <!-- End Container fluid -->
        <!-- Dots -->
        <div class="dots d-flex justify-content-center align-items-center mt-5">
            <div class="dot active mx-2"></div>
            <div class="dot mx-2"></div>
            <div class="dot mx-2"></div>
            <div class="dot mx-2"></div>
        </div>
        <!-- End Dots -->
    </div>
    <!-- End Reviews -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.reviews {
    background-color: $jumbotron-background;
    padding: 4rem 0;

    h5 {
        color: $main-green;
    }

    h2 {
        font-weight: 700;
        margin: 1rem 0;
    }
}

.ms_card {
    background-color: white;
    padding: 2rem 2.5rem 3rem;

    h6 {
        font-weight: 600;
    }

    p {
        font-size: .9rem;
        margin: 1rem 0 2rem;
    }

    &.opaque {
        opacity: 0.4;
    }
}


.user {
    img {
        height: 60px;
        width: 60px;
        border-radius: 50%;
        margin-right: 1rem;
    }

    .name {
        font-size: .9rem;
        font-weight: 600;
    }

    .work {
        font-size: .8rem;
        margin-top: 10px;
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
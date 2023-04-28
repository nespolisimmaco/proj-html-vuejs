<script>
export default {
    name: "AppFooter",
    props: {
        addresses: Array,
        explore: Array,
        links: Array,
        information: Array
    },
    data() {
        top: 0
    },
    methods: {
        scrollTop() {
            window.scrollTo(0, this.top);
        }
    }
}
</script>

<template>
    <footer>
        <button @click="scrollTop"><i class="fa-solid fa-arrow-up-long"></i></button>
        <!-- Container -->
        <div class="ms_container">
            <!-- Container fluid -->
            <div class="container-fluid">
                <!-- Row -->
                <div class="row">
                    <!-- Column -->
                    <div class="col-4">
                        <!-- Address -->
                        <div class="address">
                            <h5>Address</h5>
                            <!-- Address links -->
                            <nav>
                                <ul>
                                    <li v-for="(address, index) in addresses" :key="index">
                                        <a href="#">{{ address }}</a>
                                    </li>
                                </ul>
                                <div class="socials">
                                    <ul class="d-flex">
                                        <li class="me-3">
                                            <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
                                        </li>
                                        <li class="me-3">
                                            <a href="#"><i class="fa-brands fa-twitter"></i></a>
                                        </li>
                                        <li class="me-3">
                                            <a href="#"><i class="fa-brands fa-instagram"></i></a>
                                        </li>
                                        <li class="me-3">
                                            <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                                        </li>
                                    </ul>
                                </div>
                            </nav>
                            <!-- End Address links -->
                        </div>
                        <!-- End Address -->
                    </div>
                    <!-- End Column -->

                    <!-- Column -->
                    <div class="col-7">
                        <!-- Wrapper -->
                        <div class="d-flex justify-content-end">
                            <!-- Explore -->
                            <div class="explore">
                                <h5>Explore</h5>
                                <!-- Row -->
                                <div class="row row-cols-2">
                                    <!-- Column -->
                                    <div class="col">
                                        <div class="links">
                                            <ul>
                                                <li v-for="(link, index) in explore" :key="index">
                                                    <a href="#">{{ link }}</a>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <!-- End Column -->
                                    <!-- Column -->
                                    <div class="col">
                                        <div class="links">
                                            <ul>
                                                <li v-for="(link, index) in links" :key="index">
                                                    <a href="#">{{ link }}</a>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <!-- End Column -->
                                </div>
                                <!-- End Row -->
                            </div>
                            <!-- End explore -->
                            <!-- Information -->
                            <div class="information">
                                <h5>information</h5>
                                <ul>
                                    <li v-for="(link, index) in information" :key="index">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>
                            <!-- End nformation -->
                        </div>
                        <!-- End Wrapper -->
                    </div>
                    <!--End  Column -->
                </div>
                <!-- End Row -->
            </div>
            <!-- End Container fluid -->
            <div class="copyright text-center">
                &copy; 2020Maxcoach. All Rights Reserved
            </div>
        </div>
        <!-- End Container -->
    </footer>
</template>


<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

footer {
    background-color: $footer-blue;
    padding: 3rem 0;
    color: white;
    position: relative;

    button {
        background-color: $main-green;
        border: none;
        border-radius: 50%;
        color: white;
        width: 50px;
        height: 50px;
        position: absolute;
        bottom: 1rem;
        right: 1rem;
        transition: all 0.3s;

        &:hover {
            background-color: $hover-button;
        }
    }

    ul {
        padding: 0;

        li {
            list-style-type: none;
            margin: 10px 0;
            font-size: .8rem;

            a {
                color: $footer-links;
                text-decoration: none
            }
        }
    }
}

.ms_container {
    @include ms_container();
}

.socials {
    ul {
        li {
            font-size: 1.2rem;
        }
    }
}

.explore {
    width: 55%;
}

.copyright {
    font-size: .8rem;
    color: $footer-links;
}
</style>
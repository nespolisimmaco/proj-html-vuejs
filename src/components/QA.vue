<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "QA"
}
</script>

<template>
    <!-- Q&A -->
    <div class="QA">
        <img id="dots" src="../assets/img/maxcoach-shape-07-150x150.png">
        <!-- Container -->
        <div class="container d-flex justify-content-start">
            <!-- Video -->
            <div class="video d-flex align-items-center me-5">
                <img class="video-poster" src="../assets/img/home-business-video-poster-670x450.jpg" alt="Video poster">
                <img class="youtube-icon" src="../assets/img/icon-youtube-play.png" alt="Youtube icon">
            </div>
            <!-- Question and answers -->
            <div class="questions ms-5">
                <h2>To Thrive in Business Today, You'll Need a Good Plan</h2>
                <!-- Questions list -->
                <ul class="ps-0">
                    <li>
                        <h5>How can we help?</h5>
                        <p>How many courses you've been on, using however many techniques and methods. Unless you've come to
                            realize the value of mindset, then you've yet to understand how succesa comes.</p>
                        <p>With everyone else's mindset involved impacting too. Hence why business coaching is so crucial
                            for success.</p>
                    </li>
                    <li>
                        <h5>Why would I need a business COACH?</h5>
                        <p>How many courses you've been on, using however many techniques and methods. Unless you've come to
                            realize the value of mindset, then you've yet to understand how succesa comes.</p>
                        <p>With everyone else's mindset involved impacting too. Hence why business coaching is so crucial
                            for success.</p>
                    </li>
                    <li>
                        <h5>What is one-on-one coaching?</h5>
                        <p>How many courses you've been on, using however many techniques and methods. Unless you've come to
                            realize the value of mindset, then you've yet to understand how succesa comes.</p>
                        <p>With everyone else's mindset involved impacting too. Hence why business coaching is so crucial
                            for success.</p>
                    </li>
                </ul>
                <!-- End Questions list -->
            </div>
        </div>
        <!-- End Container -->
    </div>
    <!-- End Q&A -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.QA {
    background-color: $QA-blue;
    padding: 5.5rem 0;
    position: relative;
    background-image: url("../assets/img/background-map-dots-top-right-transparent.png");
    background-repeat: no-repeat;
    background-position: right 0 top 0;

    .container {
        padding-left: 40px;
    }

    .video {
        position: relative;

        .video-poster {
            height: 350px;
        }

        .youtube-icon {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }

    .questions {
        color: white;
        width: 35%;

        h2 {
            font-weight: 600;
        }

        // List items
        li {
            background-color: transparent;
            color: white;
            border-bottom: 1px solid grey;
            list-style-type: none;
            cursor: pointer;

            h5 {
                margin: 1.5rem 0;
                display: inline-block;

                &::before {
                    display: inline-block;
                    content: '\f0d7';
                    font-family: FontAwesome;
                    font-weight: normal;
                    font-style: normal;
                    border: 3px solid white;
                    border-radius: 50%;
                    width: 30px;
                    height: 30px;
                    text-align: center;
                    margin-right: 1rem;
                }
            }

            p {
                font-size: .8rem;
                display: none;
            }

            &:hover {
                h5 {
                    color: $main-green;

                    &::before {
                        content: '\f0d8';
                        border-color: $main-green;
                    }
                }

                p {
                    display: block;
                }
            }
        }
    }

    #dots {
        position: absolute;
        bottom: 0;
        left: 30px;
    }
}
</style>
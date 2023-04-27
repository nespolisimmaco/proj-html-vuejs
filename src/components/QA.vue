<script>
export default {
    data() {
        return {}
    }
}
</script>

<template>
    <!-- Q&A -->
    <div class="QA">
        <!-- Container -->
        <div class="container d-flex justify-content-center">
            <!-- Video -->
            <div class="video d-flex align-items-center me-5">
                <img class="video-poster" src="../assets/img/home-business-video-poster-670x450.jpg" alt="Video poster">
                <img class="youtube-icon" src="../assets/img/icon-youtube-play.png" alt="Youtube icon">
            </div>
            <!-- Question and answers -->
            <div class="questions ms-5">
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati aliquam sint sequi tempore deleniti
                    illum consequatur. Esse in blanditiis atque quas sunt facilis, recusandae illum, vitae, totam id earum
                    aut sit. Doloremque earum est at inventore eius, ratione odit quisquam molestias. Ut sequi, obcaecati ea
                    eligendi impedit, ipsa quo eos atque cupiditate esse, nostrum ipsum ipsam similique eius ab dolorum est
                    rem aut saepe eaque laboriosam? Vero magni minima quis explicabo laboriosam laudantium quasi. Ab a est
                    consectetur maxime ullam dolor nihil temporibus itaque. Molestias illum velit reprehenderit incidunt
                    exercitationem optio, nesciunt, culpa repudiandae explicabo officia veritatis debitis vel asperiores.
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis ratione sequi eos non quos accusamus
                    eaque explicabo esse alias ducimus.
                </p>
            </div>
        </div>
        <!-- End Container -->
    </div>
    <!-- Q&A -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.QA {
    background-color: $QA-blue;
    padding: 5rem 0;

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
        width: 30%;
    }
}
</style>
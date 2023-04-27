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
            <div class="video me-5">
                <img src="../assets/img/home-business-video-poster-670x450.jpg" alt="Video poster">
            </div>
            <!-- Question and answers -->
            <div class="questions ms-5">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus expedita cum itaque esse.
                    Eaque voluptas accusantium eveniet quia quam ducimus illum fugit laborum, fuga excepturi facilis
                    sed, repudiandae dolor commodi?</p>
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
        img {
            height: 300px;
        }
    }

    .questions {
        color: white;
        width: 35%;
    }
}
</style>
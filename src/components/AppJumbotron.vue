<script>
export default {
    name: "AppJumbotron",
    data() {
        return {

        }
    }
}
</script>
        
<template>
    <!-- Jumbotron -->
    <div class="jumbotron">
        <!-- Container -->
        <div class="ms_container d-flex justify-content-between">
            <!-- Jumbotron text -->
            <div class="jumbotron-text">
                <h5>New Challenges, New Skills</h5>
                <h2 class="my-4">BUILD YOUR OWN LIFE COACHING BUSINESS</h2>
                <p>Whole-Life Business Coaching for committed entrepreneurs</p>
                <button class="btn mt-2">Get started today</button>
            </div>
            <!-- Jumbotron image -->
            <div class="jumbotron-image">
                <img src="../img/home-business-hero-avatar.png" alt="Man">
            </div>
        </div>
        <!-- End Container -->
        <!-- Tools -->
        <div class="tools d-flex flex-column justify-content-around align-items-center">
            <a href="#"><i class="fa-solid fa-ruler-combined"></i></a>
            <a href="#"><i class="fa-solid fa-life-ring"></i></a>
            <a href="#"><i class="fa-solid fa-book"></i></a>
            <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
        </div>
    </div>
    <!-- End Jumbotron -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.jumbotron {
    background-color: $jumbotron-background;
}

.ms_container {
    @include ms_container();
}

.jumbotron {
    position: relative;

    &-text {
        width: 40%;
        padding: 8rem 0;

        h5 {
            color: $main-green;
            font-weight: 600;
        }

        h2 {
            font-weight: 900;
            font-size: 2.5rem;
        }

        p {
            font-weight: 600;
            color: grey;
            font-size: .9rem;
        }

        button {
            background-color: $main-green;
            color: white;
            font-weight: 600;
            font-size: .8rem;
            padding: 10px 2rem;
        }

    }

    &-image {
        width: 60%;
        background-image: url(../img/home-business-hero-global-image.png);
        background-size: cover;
        padding-top: 2rem;
        padding-left: 1rem;
        position: relative;

        img {
            height: 550px;
            position: absolute;
            bottom: 0;
            left: 2rem;
        }
    }
}

.tools {
    background-color: white;
    position: absolute;
    right: 0;
    top: 100px;
    border-radius: 5px;
    padding: 5px;

    a {
        color: inherit;
        margin: 5px 0;
    }
}
</style>
<script>
export default {
    name: "Newsletter",
}
</script>

<template>
    <!-- Newsletter -->
    <div class="newsletter text-center">
        <img id="dots" src="../assets/img/maxcoach-shape-09.png">
        <img id="circle" src="../assets/img/maxcoach-shape-02.png">
        <!-- Container -->
        <div class="ms_smaller-container">
            <h2>Subscribe <span>Newsletters</span></h2>
            <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            <!-- Input group -->
            <div class="input-group mb-3">
                <input type="email" class="form-control" placeholder="Enter your email" aria-label="Enter your email"
                    aria-describedby="button-addon2">
                <button class="btn" type="button" id="button-addon2">Subscribe</button>
            </div>
            <!-- End Input group -->
        </div>
        <!-- End Container -->
    </div>
    <!-- End Newsletter -->
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.newsletter {
    padding: 4rem 0;
    position: relative;

    #dots {
        position: absolute;
        top: 50px;
        right: 200px;
    }

    #circle {
        position: absolute;
        top: 130px;
        right: 200px;
    }
}

.ms_smaller-container {
    width: 30%;
    margin: 0 auto;
    max-width: 600px;

    h2 {
        font-weight: 600;

        span {
            font-weight: 400;
            color: $main-green;
        }
    }

    p {
        font-size: .8rem;
        font-weight: 600;
        color: grey;
        margin: 1rem 0 2.5rem;
    }
}

.input-group {
    input {
        background-color: $jumbotron-background;
        font-size: .8rem;
        padding: 10px;
    }

    button {
        background-color: $main-green;
        color: white;
        font-weight: 700;
        font-size: .8rem;

        &:hover {
            background-color: $hover-button;
        }
    }
}
</style>
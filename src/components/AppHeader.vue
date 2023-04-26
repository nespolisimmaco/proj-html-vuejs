<script>
import { store } from "../store";
import "@fortawesome/fontawesome-free/css/all.css"

export default {
    name: "AppHeader",
    props: {
        links: Array
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <header>
        <!-- Container -->
        <div class="ms_container d-flex justify-content-between align-items-center h-100">
            <!-- Logo -->
            <div class="logo text-end">
                <a href="#">
                    <img src="../img/dark-logo.png" alt="MaxCoach logo">
                </a>
            </div>
            <!-- Links -->
            <div class="links d-flex justify-content-center flex-grow-1">
                <nav>
                    <ul class="d-flex mb-0">
                        <li v-for="(link, index) in links" :key="index">
                            <a href="#">{{ link }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
            <!-- Language and Search field -->
            <div class="header-input d-flex align-items-center w-25 h-100">
                <!-- Language -->
                <div class="language d-flex justify-content-center align-items-center w-50 h-100">
                    <!-- Flags -->
                    <img v-if="store.chosenLanguage == 'english'" src="../img/en.png" alt="English">
                    <img v-if="store.chosenLanguage == 'french'" src="../img/fr.png" alt="Frecnh">
                    <img v-if="store.chosenLanguage == 'deutsch'" src="../img/de.png" alt="Deutsch">
                    <!-- Select language -->
                    <select class="mx-2" name="languages" id="languages" v-model="store.chosenLanguage">
                        <option value="english">ENGLISH</option>
                        <option value="french">FRENCH</option>
                        <option value="deutsch">DEUTSCH</option>
                    </select>
                    <i class="fa-regular fa-circle-user"></i>
                </div>
                <!-- End Language -->

                <!-- Search -->
                <div class="search-bar w-50">
                    <div class="input-group">
                        <input type="text" class="form-control" placeholder="Search..." aria-label="Search"
                            aria-describedby="button-addon2">
                        <button class="btn" type="button" id="button-addon2"><i
                                class="fa-solid fa-magnifying-glass"></i></button>
                    </div>
                </div>
                <!-- End Search -->
            </div>
        </div>
        <!-- End Container -->
    </header>
</template>


<style scoped lang="scss">
header {
    height: 80px;
    border: 1px solid black;
}

// Logo
.logo {
    width: 20%;

    img {
        height: 30px;
    }
}

// Links
.links {
    li {
        list-style-type: none;
        margin: 0 1.3rem;
        font-size: .8rem;
        font-weight: 500;

        a {
            text-decoration: none;
            color: inherit;

            &::after {
                content: '\f078';
                font-family: FontAwesome;
                font-weight: normal;
                font-style: normal;
                font-size: .5rem;
                vertical-align: middle;
                margin-left: 5px;
            }
        }
    }
}

// Language and search bar
.language {
    border-right: 1px solid lightgrey;

    select {
        border: none;
        font-size: .9rem;
        font-weight: 600;
    }
}

.header-input {
    .search-bar {
        input {
            border: none;
        }
    }
}
</style>
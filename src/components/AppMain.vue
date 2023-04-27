<script>
import AppJumbotron from './AppJumbotron.vue';
import CompanyFeatures from './CompanyFeatures.vue';
import CompanyServices from './CompanyServices.vue';
import CompanyCourses from './CompanyCourses.vue';
export default {
    name: "AppMain",
    components: {
        AppJumbotron,
        CompanyFeatures,
        CompanyServices,
        CompanyCourses
    },
    data() {
        return {

        }
    }
}
</script>
        
<template>
    <main>
        <AppJumbotron />
        <CompanyFeatures />
        <CompanyServices />
        <CompanyCourses />
    </main>
</template>


<style lang="scss" scoped></style>
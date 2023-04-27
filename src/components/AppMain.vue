<script>
import AppJumbotron from './AppJumbotron.vue';
import CompanyFeatures from './CompanyFeatures.vue';
import CompanyServices from './CompanyServices.vue';
export default {
    name: "AppMain",
    components: {
        AppJumbotron,
        CompanyFeatures,
        CompanyServices
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
    </main>
</template>


<style lang="scss" scoped></style>
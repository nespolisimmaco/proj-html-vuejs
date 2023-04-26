<script>
import AppJumbotron from './AppJumbotron.vue';
import CompanyFeatures from './CompanyFeatures.vue';
export default {
    name: "AppMain",
    components: {
        AppJumbotron,
        CompanyFeatures
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
    </main>
</template>


<style lang="scss" scoped></style>
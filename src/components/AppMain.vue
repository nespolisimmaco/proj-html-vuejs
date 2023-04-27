<script>
import AppJumbotron from './AppJumbotron.vue';
import CompanyFeatures from './CompanyFeatures.vue';
import CompanyServices from './CompanyServices.vue';
import CompanyCourses from './CompanyCourses.vue';
import QA from './QA.vue';
export default {
    name: "AppMain",
    components: {
        AppJumbotron,
        CompanyFeatures,
        CompanyServices,
        CompanyCourses,
        QA
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
        <QA />
    </main>
</template>


<style lang="scss" scoped></style>
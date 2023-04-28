<script>
import AppJumbotron from './AppJumbotron.vue';
import CompanyFeatures from './CompanyFeatures.vue';
import CompanyServices from './CompanyServices.vue';
import CompanyCourses from './CompanyCourses.vue';
import QA from './QA.vue';
import UpcomingEvents from './UpcomingEvents.vue';
import Reviews from './Reviews.vue';
import Newsletter from './Newsletter.vue';

export default {
    name: "AppMain",
    components: {
        AppJumbotron,
        CompanyFeatures,
        CompanyServices,
        CompanyCourses,
        QA,
        UpcomingEvents,
        Reviews,
        Newsletter
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
        <UpcomingEvents />
        <Reviews />
        <Newsletter />
    </main>
</template>


<style lang="scss" scoped></style>
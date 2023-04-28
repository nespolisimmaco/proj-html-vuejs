<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      // Header
      headerLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
      // Footer
      footerAddress: ["382 NE 191st St # 87394 Miami, FL 33179-3899", "+1 (305) 547-9909 (9am-5pm EST, Monday-Friday)", "support@maxcoach.com"],
      exploreLinks: ["Start here", "Blog", "About us"],
      footerLinks: ["Success story", "Courses", "Contact us"],
      informationLinks: ["Membership", "Purchase guide", "Privacy policy", "Terms of service"]
    }
  }
}
</script>
    
<template>
  <div>
    <AppHeader :links="headerLinks" />
    <AppMain />
    <AppFooter :addresses="footerAddress" :explore="exploreLinks" :links="footerLinks" :information="informationLinks" />
  </div>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
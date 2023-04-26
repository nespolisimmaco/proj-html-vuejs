<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain
  },
  data() {
    return {
      headerLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"]
    }
  }
}
</script>
    
<template>
  <div>
    <AppHeader :links="headerLinks" />
    <AppMain />
  </div>
</template>


<style lang="scss">
@use "./style/general.scss";
</style>
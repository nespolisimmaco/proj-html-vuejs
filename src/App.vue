<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader
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
  </div>
</template>


<style lang="scss">
@use "./style/general.scss";
</style>
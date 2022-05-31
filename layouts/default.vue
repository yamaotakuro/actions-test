<template>
  <div id="page" :class="{result:currentPage}">
    <Header />
    <main class="l-main">
      <Nuxt />
    </main>
    <Footer />
  </div>
</template>


<script lang="ts">
import Vue from 'vue';
import Header from '@/components/TheHeader.vue';
import Footer from '@/components/TheFooter.vue';

export default Vue.extend({
  components: {
    Header,
    Footer,
  },
  computed: {
    currentPage () {
      if(this.$route.name === 'result'){
        return true
      }else{
        return false
      }
    }
  }
});
</script>

<style lang="scss">
@use '@/assets/sass/foundation/' as f;

#page {
  position: relative;
}
.l-main {
}
</style>

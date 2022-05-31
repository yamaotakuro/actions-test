<template>
  <ul class="c-posts_archive">

  </ul>
</template>

<script lang="ts">
import Types from '@/types'
import axios from 'axios'
import Vue from 'vue'

export default Vue.extend({
  // data() {
    //   return {
      //     posts: {},
  //   };
  // },
  // created () {
    //   axios.get('http://static-test-com.check-wpx.jp/wp-json/wp/v2/custom_posts')
  //     .then((res) => {
    //       this.posts = res.data
  //     })
  // },

  // asyncData () {
  //   return axios.get('http://static-test-com.check-wpx.jp/wp-json/wp/v2/custom_posts')
  //     .then((res) => {
  //       return { posts: res.data }
  //   })
  // },
})
// const { data: posts } = await useFetch<Types.Posts>('http://static-test-com.check-wpx.jp/wp-json/wp/v2/custom_posts')

</script>

<style scoped lang="scss">
@use '@/assets/sass/foundation' as f;
.c-posts_archive{
  display: flex;
  margin-left: f.smooth_size(-5px , -10px);
  margin-right: f.smooth_size(-5px , -10px);
}
.c-post_block{
  width: 20%;
  padding: f.smooth_size( 5px, 10px);
  &__thumb{
    margin-bottom: f.smooth_size(5px , 10px);
  }
  &__title{
    font-size: f.smooth_font(15px , 18px);
  }
}
</style>
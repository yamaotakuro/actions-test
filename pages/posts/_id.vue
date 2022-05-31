<template>
  <div class="single">{{ article.title }}</div>
</template>

<script lang="ts">
import Types from '@/types'
import axios from 'axios'
import Vue from 'vue'
export default Vue.extend({
  // data() {
  //   return {
  //     article: {} as Types.PostSingle,
  //   };
  // },
  async asyncData({ app, route}) {
      const response = await app.$axios.get(`http://static-test-com.check-wpx.jp/wp-json/wp/v2/posts/${route.params.id}`)
      return {
        article: response.data
      }
    }
})
</script>

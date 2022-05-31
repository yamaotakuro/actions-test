<template>
  <div class="p-index">
    <section class="p-index_kv">
      <TheKvSlider/>
    </section>
    <section class="p-index_contents">
      <div class="c-container">
        <h2 class="p-index_contents__title">てすと</h2>
        <!-- <ThePostsBlock/> -->
        <ul class="c-posts_archive">
          <li class="c-post_block" v-for="(post,index) in posts" :key="index">
            <NuxtLink :to="`/posts/${post.id}`">
            <div class="c-post_block__thumb">
              <img :src="`${post.thumb}`" alt="" />
            </div>
            <h3 class="c-post_block__title">{{ post.title }}</h3>
            </NuxtLink>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TheKvSlider from '@/components/TheKvSlider.vue';
import ThePostsBlock from '@/components/ThePostsBlock.vue';
export default Vue.extend({
  name: 'IndexPage',
  components: {
    TheKvSlider,
    ThePostsBlock
  },
  async asyncData({ app }) {
    const response = await app.$axios.get('http://static-test-com.check-wpx.jp/wp-json/wp/v2/custom_posts')
    return {
      posts: response.data
    }
  }
})
</script>

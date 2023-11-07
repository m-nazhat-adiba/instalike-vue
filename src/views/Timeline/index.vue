<script setup lang="js">
import Layout from '../../components/common/layout/Layout.vue'
import PostCard from '../../components/timeline/postcard/PostCard.vue'
import StoryCard from '../../components/timeline/story/StoryCard.vue'
import { onMounted, ref } from 'vue'
import axios from 'axios'

const postData = ref(null)

const fetchData = async () => {
  try {
    const response = await axios.get('https://jsonplaceholder.typicode.com/photos')
    postData.value = response.data
  } catch (error) {
    console.log('error', error)
  }
}

onMounted(fetchData)
</script>

<template>
  <Layout>
    <!-- Story Start -->
    <section class="flex justify-between px-5 my-4">
      <StoryCard />
      <StoryCard />
      <StoryCard />
      <StoryCard />
    </section>
    <!-- Story End -->

    <section class="flex flex-col gap-10 my-10">
      <PostCard v-for="item in postData" v-bind:key="item.id" :title="item.title" :url="item.url" />
    </section>
  </Layout>
</template>

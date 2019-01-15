<template>
  <section class="container">
    <PostPreview 
      v-for="post in posts" 
      :key="post.id" 
      :title="post.title" 
      :excerpt="post.previewText" 
      :thumb="post.img"
      :id="post.id" />
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: 'Maunsell Forts',
          previewText: 'Maunsell Forts, Thames Estuary, WW2',
          img:
            'https://theromneymarsh.net/assets/fileman/Uploads/History/buildings/Sound%20Mirrors/30_Foot_Sound_Mirror_2015.jpg',
          id: 'maunsell-forts'
        },
        {
          title: 'La Coupole',
          previewText: 'La Coupole, France WW2',
          img:
            'https://theromneymarsh.net/assets/fileman/Uploads/History/buildings/Sound%20Mirrors/30_Foot_Sound_Mirror_2015.jpg',
          id: 'la-coupole-france'
        }
      ]
    }
  }
}
</script>

<style>
</style>

<template>
  <nuxt-link 
    :to="id">
    <article class="post-preview">
      <div 
        :style="{backgroundImage: 'url(' + thumb + ')'}" 
        class="post-preview-thumb" />
      <div class="post-preview-content">
        <div class="post-title">{{ title }}</div>
        <div class="post-excerpt">{{ excerpt }}</div>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    thumb: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: #222;
}

.post-preview {
  margin: 1rem;
  width: 90%;
  height: 20rem;
  border-radius: 3px;
  box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.5);
}

.post-preview-thumb {
  width: 100%;
  height: 10rem;
  background-position: center;
  background-size: cover;
}

.post-preview-content {
  padding: 1rem;
  text-align: center;
}

.post-title {
  margin-bottom: 1rem;
  font-size: 1.5rem;
  line-height: 1.5;
  font-weight: bold;
}

.post-excerpt {
  margin-bottom: 1rem;
  font-size: 1rem;
  line-height: 1.5;
}

@media (min-width: 35rem) {
  .post-preview {
    width: 25rem;
    margin: 1rem;
  }
}
</style>

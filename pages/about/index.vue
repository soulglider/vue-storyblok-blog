<template>
  <section id="about-page">
    <h1>{{ title }}</h1>
    <p>{{ content }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return context.app.$storyapi
      .get('cdn/stories/about', {
        version: 'draft'
      })
      .then(res => {
        console.log(res.data)
        return {
          title: res.data.story.content.title,
          content: res.data.story.content.content
        }
      })
  }
}
</script>

<style scoped>
#about-page {
  width: 90%;
  max-width: 640px;
  margin: auto;
  padding: 2rem 0;
}

h1 {
  margin-bottom: 1rem;
}

p {
  white-space: pre;
}
</style>

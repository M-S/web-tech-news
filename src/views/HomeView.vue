<script setup lang="ts">
import TheWelcome from '../components/TheWelcome.vue'
const articleList = [
  {
    id: 1,
    title: 'The ultimate guide to Vue 3',
    content:
      "The new version of Vue.js has been released! It's packed with new features to help you write better code faster. In this article, we'll explore some of the most exciting ones and show you how they can make your life easier."
  },
  {
    id: 2,
    title: 'Tech trends for 2024',
    content:
      "The future is now! We're living in a world where technology is advancing at an exponential rate. In this article, we'll explore some of the most exciting tech trends that will be shaping our lives over the next few years."
  },
  {
    id: 3,
    title: 'AI gets smarter',
    content:
      'Artificial intelligence is getting smarter every day. In this article, we will explore the latest advancements in AI and how they are changing our world for the better.'
  },
  {
    id: 4,
    title: 'Best practices for code reviews',
    content:
      'Code reviews are a great way to improve the quality of your code. In this article, we will discuss best practices for conducting code reviews and how you can use them to make sure that your team is producing high-quality code.'
  },
  {
    id: 5,
    title: 'How to get started with machine learning',
    content:
      'Machine learning is a powerful tool that can be used to solve many problems. In this article, we will explore how you can get started with machine learning and what the future holds for this exciting field of study.'
  }
]
</script>

<template>
  <main>
    <TheWelcome />
    <div class="articles">
      <div class="article-wrapper" v-for="(article, id) in articleList" :key="id">
        <h2>{{ article.title }}</h2>
        <p>{{ article.content }}</p>
        <img
          class="article-image"
          :src="`https://picsum.photos/seed/${article.id}/300/200`"
          alt="Article image"
        />
      </div>
    </div>
  </main>
</template>
<style scoped>
main {
  margin: 0 auto;
}
.articles {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  row-gap: 40px;
  column-gap: 40px;
}
.article-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-areas:
    'title'
    'content'
    'image';

  border-top: 2px solid #e0e0e0;  
  border-bottom: none;
}
.article-image {
  outline: 1px solid darkgray;
  margin: 4px 0;
  display: block;
  grid-area: image;
  width: 100%;
}
h2 {
  grid-area: title;
}
p {
  grid-area: content;
}
.article-wrapper:nth-child(3n + 2) {
  align-self: top;
  grid-template-areas:
    'image'
    'title'
    'content';
    border-top: none;
    border-bottom: none;
}
</style>

<template>
  <div class="article-layout">
    <Header />

    <main class="article-layout-content">
      <slot></slot>
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style scoped>

.article-layout {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.article-layout-content {
  margin-top: 20px;
}
</style>

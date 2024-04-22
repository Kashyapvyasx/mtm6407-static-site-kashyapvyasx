<template>
  <div class="blog-page">
    <Header />

    <section class="blog-content">
      <h1>Location</h1>
      <div class="blog-posts">
        <p> Visit us at our nursery located in the heart of the Flower District, 456 Garden Lane, Spring Valley, CA 94122. Our doors are always open for fellow plant lovers and gardening enthusiasts.</p>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import BlogPost from '~/components/BlogPost.vue';

export default {
  components: {
    Header,
    Footer,
  },
  
  
  head() {
    return {
      title: 'GreenThumb Nursery',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Grow with Us: Cultivating Joy and Greenery.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.blog-page {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.blog-content h1 {
  font-size: 2rem;
  margin-bottom: 20px;
}

.blog-posts {
  display: grid;
  gap: 20px;
}
</style>

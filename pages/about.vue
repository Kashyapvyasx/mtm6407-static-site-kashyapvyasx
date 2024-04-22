<template>
  <div class="nursery-about-section">
    <Header />
    
    <section class="nursery-about-content">
      <h1>About GreenThumb Nursery</h1>
      <p>Founded in 2010, GreenThumb Nursery has grown from a humble plant store to a beacon for gardeners and plant enthusiasts. Learn about our journey, our team, and our vision for a greener tomorrow.</p>
    </section>
    
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
  
  head() {
    return {
      title: 'About GreenThumb Nursery',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Visit us to experience a world of plants and learn how you can make a difference, one plant at a time. Whether you’re a seasoned gardener or just starting out, GreenThumb Nursery is your partner in the journey towards a more sustainable and beautiful world.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.nursery-about-section {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.nursery-about-content h1 {
  font-size: 2rem;
  margin-bottom: 20px;
}

.nursery-about-content p {
  margin-bottom: 15px;
  line-height: 1.6;
}
</style>

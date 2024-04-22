<template>
  <div class="nursery-contact-section">
    <Header />

    <section class="nursery-contact-content">
      <h1>Get in Touch</h1>
      <p>Have questions or want to start a gardening project with us? Contact us via email at contact@greenthumbnursery.com, or call us at 555-0189. Follow us on our social media platforms for the latest updates and gardening tips.</p>
      <ContactForm />
    </section>

    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import ContactForm from '~/components/ContactForm.vue';

export default {
  components: {
    Header,
    Footer,
    ContactForm,
  },
  
  head() {
    return {
      title: 'GreenThumb Nursery',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Planting Ideas, Growing Inspiration.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.nursery-contact-section {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.nursery-contact-content h1 {
  font-size: 2rem;
  margin-bottom: 20px;
}

.nursery-contact-content p {
  margin-bottom: 15px;
  line-height: 1.6;
}
</style>

<template>
  <div class="nursery-plants-page">
    <Header />

    <section class="nursery-plants-content">
      <h1>Explore Our Plants Collection</h1>
      <div class="nursery-plant-cards">
        <PlantCard
          v-for="plant in plants"
          :key="plant.id"
          :plantName="plant.name"
          :imageSrc="plant.imageSrc"
        />
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import PlantCard from '~/components/PlantCard.vue';

export default {
  components: {
    Header,
    Footer,
    PlantCard,
  },
  
  data() {
    return {
      plants: [
        {
          id: 1,
          name: 'Ottawa',
          imageSrc: 'https://www.bestinottawa.com/wp-content/uploads/2021/06/Best-Nursery-in-Ottawa-1.jpg',
        },
        {
          id: 2,
          name: 'Alberta',
          imageSrc: 'https://ottawaroadtrips.com/wp-content/uploads/2021/05/commissioners-park-tulips-dows-lake-2021.jpg',
        },
      ],
    };
  },
  
  head() {
    return {
      title: 'GreenThumb Nursery',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Dig Deeper: Your Guide to a Greener World.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.nursery-plants-page {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.nursery-plants-content h1 {
  font-size: 2rem;
  margin-bottom: 20px;
}

.nursery-plant-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}
</style>

<template>
  <div class="nursery-home-page">
    <Header />
    
    <section class="nursery-hero">
      <h1>Welcome to GreenThumb Nursery!</h1>
      <p>Introducing GreenThumb Nursery, your partner in nurturing growth and green spaces. Discover our passion for plants and our commitment to environmental sustainability.</p>
      <a href="/plants" class="hero-btn">Explore Plants</a>
    </section>
    
    <section class="nursery-featured-plants">
      <h2>Our Work</h2>
      <div class="nursery-plant-cards">
        <PlantCard
          v-for="plant in featuredPlants"
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
      featuredPlants: [
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
          content: 'The Green Thumb Chronicles: Adventures in Gardening.',
        },
      ],
    };
  },
};
</script>

<style scoped>
.nursery-home-page {
  font-family: Arial, sans-serif;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.nursery-hero {
  text-align: center;
  padding: 100px 0;
}

.nursery-hero h1 {
  margin-bottom: 20px;
  font-size: 2.5rem;
}

.hero-btn {
  display: inline-block;
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  text-decoration: none;
  font-weight: bold;
  transition: background-color 0.3s ease;
}

.hero-btn:hover {
  background-color: #0056b3;
}

.nursery-featured-plants {
  margin-top: 40px;
  text-align: center;
}

.nursery-plant-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}
</style>

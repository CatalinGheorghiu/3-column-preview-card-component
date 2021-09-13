<template>
  <div id='app'>
    <PreviewCard v-for='car in cars'
                 :key='car.id'
                 :background-color='car.cardBgColor'
                 :description='car.description'
                 :header-title='car.carType'
                 :link='car.linkTo'>
      <template v-slot:headerIcon>
        <img :alt='`${car.carType} icon`'
             :src='require(`@/images/icon-${car.carType}.svg`)'>
      </template>
    </PreviewCard>
  </div>
</template>

<script>
import PreviewCard from './components/PreviewCard.vue';

export default {
  name: 'App',
  components: { PreviewCard },
  data() {
    return {
      cars: [
        {
          id: 1,
          carType: 'sedans',
          description: 'Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.',
          linkTo: 'www.sedans.com',
          cardBgColor: 'orange'
        },
        {
          id: 2,
          carType: 'suvs',
          description: 'Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacations and off-road adventures',
          linkTo: 'www.suvs.com',
          cardBgColor: 'light-cyan'
        },
        {
          id: 3,
          carType: 'luxury',
          description: 'Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.',
          linkTo: 'www.luxury.com',
          cardBgColor: 'dark-cyan'
        }
      ]
    };
  }
};
</script>


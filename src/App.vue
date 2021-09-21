<template>
  <div id="app" class="antialiased text-gray-900">
    <div class="bg-gray-200 min-h-screen p-1">
      <Card :property="property"/>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Card,
  },
  data: () => ({
    property: {
      imageUrl: 'https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80',
      imageAlt: 'Rear view of modern home with pool',
      beds: 3,
      baths: 2,
      title: 'Modern home in city center',
      priceInCents: 190000,
      formattedPrice: '$750,000',
      address: '742 Evergreen Terrace',
      realtorImage: 'https://v1.tailwindcss.com/_next/static/media/erin-lindford.4804b52007ca82ebe9999d19c717b44d.jpg',
      realtorName: 'tiffany heffner',
      realtorPhone: '(555)555-4321',
    },
  }),
};
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>

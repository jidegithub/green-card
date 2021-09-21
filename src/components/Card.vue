<template>
  <div class="max-w-sm m-auto">
    <div class="relative pb-5/6">
      <heart-icon class="absolute z-10 right-0 heart-icon"></heart-icon>
      <img class="absolute h-full w-full object-cover rounded-t-xl shadow-md" :src='property.imageUrl' :alt='property.imageAlt'>
    </div>
    <div class="relative">
      <div class="bg-white shadow-lg rounded-b-xl">
        <div class="p-6">
          <span class="inline-block text-sm uppercase text-gray-500 font-semibold tracking-wide">detached house &bull; 5y old</span>
          <h4 class="mt-1 font-semibold text-2xl leading-tight truncate">{{ property.formattedPrice }}</h4>
          <div class="mt-1 text-gray-600 bold">
            {{ property.address }}
          </div>
        </div>
        <div class="flex text-lg font-semibold tracking-wide border-t border-gray-100 px-6 py-5 capitalize">
          <span class="flex amenities">
            <bed-icon :iconName="bed"></bed-icon>
            <h4 class="ml-2">{{ property.beds }} <span class="text-gray-400">bedrooms</span></h4>
          </span>
          <span class="flex">
            <bath-icon :iconName="bath"></bath-icon>
            <h4 class="ml-2">{{ property.baths }} <span class="text-gray-400">bathrooms</span></h4>
          </span>
        </div>
        <div class="bg-gray-100 border-t border-gray-100 h-full rounded-b-xl">
          <div class="py-2 px-6 h-full">
            <h2 class="uppercase font-semibold text-gray-400">Realtor</h2>
            <div class="md:flex flex rounded-lg py-3">
              <img class="h-16 w-16 rounded-full mr-6 md:mx-0 md:mr-6" :src='property.realtorImage' :alt='property.realtorName'>
              <div class="md:text-left">
                <h2 class="text-lg font-semibold capitalize">{{ property.realtorName }}</h2>
                <div class="text-gray-600">{{ property.realtorPhone }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BathIcon from './icons/IconBath.vue';
import BedIcon from './icons/IconBed.vue';
import HeartIcon from './icons/IconHeart.vue';

export default {
  props: ['property'],
  components: {
    BathIcon,
    BedIcon,
    HeartIcon,
  },
};
</script>
<style scoped>
  .amenities{
    flex-grow: .4;
  }
  .heart-icon{
    top: 12px;
    right: 12px;
  }
</style>

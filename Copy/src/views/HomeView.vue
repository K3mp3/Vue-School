<script setup lang="ts">
  import sourceData from "../data.json";

  export default {
    data(){
      return {
        destinations: sourceData.destinations
      }
    }
  }
</script>

<template>
  <div class="home">
    <h1>All destinations</h1>
    <div class="destinations">
      <router-link 
        v-for="destinations in destinations" 
        :key="destinations.id" 
        :to="destinations.slug"
      >
        {{ destination.name }}
      <img :src="`/images/${destination.image}`" :alt="destination.name">
    </router-link>
    </div>
  </div>
</template>

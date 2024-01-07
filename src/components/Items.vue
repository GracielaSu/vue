<script>
export default {
    data() {
      return {
        items: [
          { name: 'Dress', description: 'You can find various styles of dresses in here' },
          { name: 'Suits', description: 'Splendid suits waiting for you to be discovered' },
          { name: 'Boutique ', description: 'Flowers make your occasion special' },
          { name: 'Rings', description: 'Unique ring designs crafted just for you' },
        ],
        showDetails: false
      };
    },
    methods: {
      toggleDetails() {
        this.showDetails = !this.showDetails;
      }
    }
  };
</script>
<template>
  <div style="display: flex;justify-content: center; text-align: center;">
    <div>
      <h3 v-for="item in items" :key="item.name" id="list-header-box">
        {{ item.name }}
        <li v-if="showDetails">{{ item.description }}</li>
      </h3>
    </div>
  </div>
</template>
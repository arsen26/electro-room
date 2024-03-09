<template>
    <v-container class="container">
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="4"
          lg="3"
          v-for="(item, index) in paginatedData"
          :key="index"

        >
          <v-card  max-width="344">
            <v-card-title>{{ item.title }}</v-card-title>
            <v-card-text>{{ item.description }}</v-card-text>
            <v-card-subtitle>Price: ${{ item.price }}</v-card-subtitle>
            <v-img :width="320"   aspect-ratio="3/4"
 :src="item.productImage"></v-img>
            <v-btn color="primary">{{ item.button }}</v-btn>
          </v-card>
        </v-col>
      </v-row>
      <v-pagination
  :length="Math.ceil(data.length / itemsPerPage)"
  v-model="currentPage"
>
</v-pagination>

    </v-container>
  </template>
  
  
  <script>
  export default {
    data() {
      return {
        currentPage: 1,
    itemsPerPage: 8,

        data: [
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),
            button: "porosit",
          },
          {
            title: "Kompjuteri numer 2",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 3",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 4",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 5",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 6",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
          {
            title: "Kompjuteri numer 1",
            description: "Pershkrimi i kompjuterit te pare",
            price: 12,
            productImage:require('@/assets/headset.png'),

            button: "porosit",
          },
        ],
      
      };
      
    },
    computed: {
  paginatedData() {
    const startIndex = (this.currentPage - 1) * this.itemsPerPage;
    const endIndex = startIndex + this.itemsPerPage;
    return this.data.slice(startIndex, endIndex);
  }
}
  };
  </script>
  
  <style scoped>
    

</style>
  
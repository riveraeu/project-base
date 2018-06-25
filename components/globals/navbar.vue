<template>
  <div class="">
    <v-toolbar fixed app>
      <v-toolbar-side-icon class="hidden-md-and-up" v-on:click="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-items class="ml-0">
        <v-btn flat to="/" color="">
          <v-icon ></v-icon>
          <v-toolbar-title class=""></v-toolbar-title>
        </v-btn>
      </v-toolbar-items>
      <v-spacer/></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down mr-0">
        <v-btn flat v-for="(link, index) in navigation" :key="index" :to="link.to" color="">
          <v-icon left>{{link.icon}}</v-icon>{{link.title}}</v-btn>
        <!-- Shoppoing cart icon
        <v-btn v-show="showCart" flat to="/lights/rentals/cart">
          <v-badge right overlap>
            <span slot="badge">{{ cartTotal }}</span>
            <v-icon large color="grey">shopping_cart</v-icon>
          </v-badge>
        </v-btn> -->
      </v-toolbar-items>
    </v-toolbar>
    <!-- mobile side nav menu -->
    <v-navigation-drawer temporary v-model="drawer" fixed>
      <!-- Shoppoing cart icon
      <v-btn class="mt-3" v-show="showCart" flat to="/lights/rentals/cart">
        <v-badge overlap>
          <span slot="badge">{{ cartTotal }}</span>
          <v-icon large color="grey">shopping_cart</v-icon>
        </v-badge>
      </v-btn>
      <v-divider></v-divider> -->
      <div class="" v-for="(link, index) in navigation" :key="index">
        <v-list-tile color="" avatar :to="link.to">
          <v-list-tile-avatar>
            <v-icon class="">{{link.icon}}</v-icon>
         </v-list-tile-avatar>
         <v-list-tile-content>
           <v-list-tile-title class="">{{link.title}}</v-list-tile-title>
         </v-list-tile-content>
       </v-list-tile>
       <v-divider></v-divider>
      </div>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      navigation: [
        {title: '', to: '', icon: ''},
        {title: '', to: '', icon: ''},
        {title: '', to: '', icon: ''}
      ]
    }
  },
  /* Shoppoing cart stuff
  computed: {
    cartTotal () {
      return this.$store.state.rentals.cartTotal
    },
    showCart () {
      return this.$store.state.rentals.showCart
    }
  }
  */
}
</script>

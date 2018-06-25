<template>
  <v-flex v-on:mouseover="active = true" v-on:mouseleave="active =
  false" class="box" sm6 text-xs-center>
    <nuxt-link :to="{name: '', params: {: }}">
      <img :src="" :alt="">
      <div v-show="active" class="image-overlay">
        <h3 class="image-title display-1"> {{ }}</h3>
      </div>
    </nuxt-link>
  </v-flex>
</template>

<script>
export default {
  props: [''],
  data () {
    return {
      active: false
    }
  }
}
</script>

<style scoped>
.box {
  position: relative;
}
.image-overlay {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: rgba(38, 50, 56, 0.7);
  display: table;
}
.image-title {
  display: table-cell;
  vertical-align: middle;
}
</style>

<template>
  <div class="img-illustration">
    <div class="img-container">
      <img :src="require(`./../../assets/${img}`)" alt="dummy image" />
    </div>
  </div>
</template>

<script>
export default {
  props: ['imgSrc'],
  computed: {
    img: function() {
      return this.imgSrc;
    },
  },
  data: function() {
    return {
    }
  },
  methods: {}
}
</script>

<style>
</style>
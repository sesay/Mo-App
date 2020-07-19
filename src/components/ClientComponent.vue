<template>
  <div class="client">
    <div class="client-wrapper">
      <img src="./../assets/client.png" alt="">
    </div>
  </div>
</template>

<script>
// import SectionComponent from './../SharedComponent/SectionComponent/SectionComponent'

import data from './../model/data';

export default {
  components: {
    // SectionComponent,
  },
  data: function() {
    return {
      data: data.client,
    }
  },
  methods: {
  }
}
</script>

<style>
  .client {
    margin-top: 290px;
    margin-left: 240px;
  }

  .client-wrapper {
    max-width: 1360px;
    width: 100%;
  }

  .client .content-box-desc {
    font-family: 'DM Serif Display', sans-serif;
    font-size: 48px;
    line-height: 67px;
  }
</style>
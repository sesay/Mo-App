<template>
  <div class="header">
    <NavigationComponent :nav="homeNav" />
    <section class="header-title">
      <h2 v-html="subHeader"></h2>
      <a href="#" class="btn">get started <i class="arrow"></i></a>
    </section>
  </div>
</template>

<script>
import NavigationComponent from './NavigationComponent'
import data from './../model/data'

export default {
  components: {
    NavigationComponent
  },
  data: function() {
    return { 
      homeNav: data.homepage.navigation,
      subHeader: data.homepage.subHeader
    }
  },
  methods: {}
}
</script>

<style>
  .header {
    background: url('./../assets/header-bg.png') no-repeat;
    background-size: cover;
    height: auto;
    max-width: 1285px;
    padding-left: 240px;
    padding-top: 50px;
    padding-bottom: 36%;
  }

   .header .navigation {
    margin-right: -62px;
    margin-top: -8px;
  }

  .header .navigation li:last-child a {
    background: #EE4D47;
    border-radius: 5px;
    font-weight: 500;
    padding: 20px 25px;
    line-height: 19px;
  }

  .header .navigation-component li:not(:last-child) a {
    margin-right: 93px;
  }

  .header-title {
    color: #fff;
    margin-top: 90px;
  }
  .header-title h2 {
    font-size: 100px;
    font-family: 'DM Serif Display', sans-serif;
    line-height: 100%;
  }

  .header-title a {
    color: #fff;
    text-transform: uppercase;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    margin-top: 60px;
    background: #EE4D47;
    border-radius: 5px;
    min-width: 220px;
    height: 60px;
    color: #fff;
    font-weight: bold;
    font-size: 16px;
    line-height: 19px;
    border: 0;
  }

  .header-title a > i {
    display: inline-block;
    width: 29px;
    height: 12px;
    background:url('./../assets/arrow.png') no-repeat;
    background-size: contain;
    margin-left: 20px;
  }
</style>
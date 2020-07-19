<template>
  <div class="navigation-component">
    <div class="logo">
      <img src="./../assets/logo.png" alt="trafico">
    </div>
    <nav class="navigation">
      <ul>
        <li v-for="(item, index) in nav" v-bind:key="index">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  props:['nav'],
  computed: { },
  data: function() {
    return {

    }
  },
  methods: {}
}
</script>

<style>
  .navigation-component {
    display: flex;
    align-items: center;
  }

  .logo {
    width: 212px;
  }

  .navigation-component .navigation {
    margin-left: auto;
    position: relative;
  }

  .navigation-component ul {
    list-style: none;
    display: flex;
    justify-content: space-between;
  }

  .navigation-component ul li a {
    text-align: center;
    text-transform: uppercase;
    color: #FFFFFF;
  }

  .navigation-component ul li:not(:last-child) a {
    margin-right: 100px;
  }
</style>
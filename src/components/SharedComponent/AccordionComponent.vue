<template>
  <div class="accordion">
    <img src="./../../assets/accordion.png" alt="accordion">
  </div>
</template>

<script>
export default {
  props:{
    accordion: {
      type: Array,
      required: true,
    }
  },
  computed: {
    title: function() {
      return this.accordion.title;
    },
    description: function() {
      return this.accordion.description;
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
  .accordion {
    max-width: 1195px;
    width: 100%;
    margin-top: -51px;
    margin-left: -35px;
  }

  .accordion input {
    position: absolute;
    opacity: 0;
    z-index: -1;
  }

  .tabs {
    overflow: hidden;
    display: flex;
    flex-flow: wrap;
    justify-content: space-between;
  }

  .tab {
    width: calc(50% - 10px);
    overflow: hidden;
    border-radius: 10px;
    margin-bottom: 10px;
    color: #402B2B;
    font-size: 18px;
    line-height: 30px;
  }

  .tab-content {
    max-height: 0;
    -webkit-transition: all .35s;
    transition: all .35s;
    display: none;
    padding: 40px 35px 60px 35px;
  }

  input:checked~.tab-content {
    max-height: 100vh;
    display: block;
  }

  .tab-label {
    display: flex;
    justify-content: space-between;
    font-weight: 500;
    cursor: pointer;
    background: #FFFFFF;
    height: 90px;
    align-items: center;
    line-height: 30px;
    padding: 0 35px;
  }

  input:checked+.tab-label::after {
    background:url('./../../assets/minus.png') no-repeat;
    background-position: center;
  }

  .tab-label::after {
    content: "";
    background:url('./../../assets/plus.png') no-repeat;
    background-size: contain;
    width: 20px;
    height: 20px;
    -webkit-transition: all .35s;
    transition: all .35s;
  }
</style>
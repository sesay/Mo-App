<template>
  <div class="about-us">
    <SectionComponent :data="data" :showQuote="showQuote" />
  </div>
</template>

<script>
import SectionComponent from './SharedComponent/SectionComponent'
import data from './../model/data';

export default {
  components: {
    SectionComponent,
  },
  data: function() {
    return {
      data: data.aboutUs,
      showQuote: true,
    }
  },
  methods: {}
}
</script>

<style>
  .about-us {
    max-width: 1170px;
    width: 100%;
    display: flex;
    margin-left: auto;
    margin-right: 160px;
    margin-top: 102px;
  }

  .about-us .content-box-desc {
    padding-top: 79px;
    position: relative;
    left: -25px;
  }

  .about-us .img-container {
    width: 575px;
    height: 480px;
    margin-left: auto;
  }

  .about-us .img-illustration {
    margin-left: auto;
  }

  .about-us .quote {
    background: rgba(252, 221, 212, 0.4);
    font-size: 24px;
    font-weight: 500;
    line-height: 36px;
    width: 100%;
    padding: 28px 60px 20px 45px;
    margin-top: 65px;
  }
</style>
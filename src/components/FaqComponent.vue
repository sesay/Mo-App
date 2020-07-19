<template>
  <div class="faq">
    <SectionComponent :data="data" />
    <AccordionComponent :accordion="accordionContent" />
  </div>
</template>

<script>
import SectionComponent from './SharedComponent/SectionComponent'
import AccordionComponent from './SharedComponent/AccordionComponent'

import data from './../model/data';

export default {
  components: {
    AccordionComponent,
    SectionComponent,
  },
  data: function() {
    return {
      data: data.faq,
      accordionContent: data.faq.accordion,
    }
  },
  methods: {
  }
}
</script>

<style>
  .faq {
    max-width: 1360px;
    margin-left: 238px;
    margin-top: 359px;
    position: relative;
  }

  .faq:after {
    content: '';
    display: block;
    width: 1170px;
    height: 100%;
    background: url('./../assets/faq-bg.png') no-repeat;
    background-size: cover;
    position: absolute;
    top: -232px;
    right: 0;
    z-index: -1;
    padding-bottom: 24.5%;
  }

  .faq .img-illustration {
    position: relative;
    top: -129px;
    left: -97px;
    max-width: 708px;
  }

  .faq .content-box-desc {
    font-family: 'DM Serif Display', sans-serif;
    font-size: 48px;
    line-height: 67px;
  }
</style>
<template>
  <div class="how-to-apply">
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
      data: data.howToApply,
      showQuote: false,
    }
  },
  methods: {
  }
}
</script>

<style>
  .how-to-apply {
    max-width: 1230px;
    width: 100%;
    margin: auto;
    margin-top: 152px;
  }

  .how-to-apply .content-box-desc {
    padding-top: 120px;
  }

  .how-to-apply .img-illustration {
    order: -1;
    top: 11px;
    left: -60px;
    position: relative;
  }

  .how-to-apply .img-container {
    width: 720px;
    height: 678px;
    margin-right: auto;
  }
</style>
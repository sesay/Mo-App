<template>
  <div class="page-section">
    <section class="content-box">
      <div class="content-box-desc">
        <h2>{{ title }}</h2>
        <p v-html="description"></p>
        <QuoteComponent :text="quote" v-show="showQuote" />
      </div>
      <ImageComponent :imgSrc="imgSrc" />
    </section>
  </div>
</template>

<script>
import QuoteComponent from './../SharedComponent/QuoteComponent'
import ImageComponent from './ImageComponent'

export default {
  props: {
    data: Object,
    showQuote: Boolean,
  },
  components: {
    ImageComponent,
    QuoteComponent
  },
  computed: {
    title: function() {
      return this.data.title
    },
    description: function() {
      return this.data.description
    },
    quote: function() {
      return this.data.quote
    },
    imgSrc: function() {
      return this.data.imgSrc
    }
  },
  data: function() {
    return {
    }
  },
  methods: {
  }
}
</script>

<style>
  .content-box {
    display: flex;
    flex-flow: row;
  }

  .content-box-desc {
    color: #402B2B;
    font-weight: 300;
    font-size: 18px;
    line-height: 40px;
    max-width: 571px;
    width: 100%;
  }

  .content-box-desc h2 {
    font-weight: bold;
    font-size: 24px;
    line-height: 40px;
    letter-spacing: 0.1em;
    color: #EE4D47;
    text-transform: uppercase;
    margin-bottom: 45px;
    font-family: 'Rubik', sans-serif;
  }
</style>
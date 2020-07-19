<template>
  <div class="quote" v-if="text">
  <p v-once v-html="text.text"></p>
</div>
</template>
<script>

export default {
  props: ['text'],
  data: function() {
    return {}
  },
  methods: {}
}
</script>

<style>
  .quote {
    border-left: 10px solid #ED4D47;
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    padding: 20px;
  }
</style>
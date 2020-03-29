<template>
  <div class="hello">
    {{ test }}
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import * as Sentry from '@sentry/browser';

export default Vue.extend({
  name: 'HelloWorld',
  props: {
    msg: String
  },
  computed: {
    test() {
      return process.env.TEST
    }
  },
  created() {
    Sentry.captureException(new Error("Test Sentry Message Second"));
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

<template>
  <div class="container">
    <app-quote-grid :quotes="myQuotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
export default {
  data: function() {
    return {
      myQuotes: ["here testing my quote"],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGrid
  }
};
</script>

<style></style>

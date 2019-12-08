<template>
  <div class="container">
    <app-new-quote @quoteAdded="NewQuote"></app-new-quote>
    <app-quote-grid :quotes="myQuotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
export default {
  data: function() {
    return {
      myQuotes: ["here testing my quote"],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  },
  methods: {
    NewQuote(quote) {
      this.myQuotes.push(quote);
    }
  }
};
</script>

<style></style>

<template>
  <div class="container">
    <app-new-quote @quoteAdded="NewQuote"></app-new-quote>
    <app-quote-grid
      :quotes="myQuotes"
      @quoteDeleted="delQuote"
    ></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          <p>Click here to delete a quote</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
export default {
  data: function() {
    return {
      myQuotes: [],
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
    },
    delQuote(index) {
      this.myQuotes.splice(index, 1);
    }
  }
};
</script>

<style></style>

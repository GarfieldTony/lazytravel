<template>
  <div class="container" id="app">
    
    <!-- <SourceSelection v-on:sourceChanged="sourceChanged"></SourceSelection>
    <Newslist v-bind:source="source"></Newslist> -->
    <BudgetSelection v-on:budgetChanged="budgetChanged"></BudgetSelection>
    <!-- <Budget></Budget> -->
    
    <div class="footer">
      <p>&copy <a href="https://www.linkedin.com/in/wu-jionghui-28844459/" target="_blank">Wu Jionghui</a> | <a href="https://www.linkedin.com/in/wu-jionghui-28844459/" target="_blank">Imprint</a></p>
    </div>
  </div>
</template>

<script>
import Newslist from './components/Newslist'
import SourceSelection from './components/SourceSelection'
import BudgetSelection from './components/BudgetSelection'
import Budget from './components/Budget'

export default {
  name: 'app',
  components: {
    Newslist,
    SourceSelection,
    BudgetSelection,
    Budget
  },
  data () {
    return {
      source: "",
      budget: ""
    }
  },
  methods: {
    sourceChanged: function (source) {
      this.source = source;
    },
    budgetChanged: function (budget) {
      this.budget = budget;
    }
  }
}
</script>

<style>
  #app {
    padding-top: 20px
  }
</style>
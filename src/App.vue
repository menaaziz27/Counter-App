<template>
  <div id="app">
    <AppTitle msg="Silly App"/>
    <CounterResult :counter="counter" />
    <IncreaseButton @IncreaseOne="plusOne"/>
  </div>
</template>

<script>
import AppTitle from './components/AppTitle.vue'
import CounterResult from './components/CounterResult';
import IncreaseButton from './components/IncreaseButton';

export default {
  name: 'App',
  components: {
    AppTitle,
    CounterResult,
    IncreaseButton
  },
  data: function() {
    return {
      counter: 0
    }
  },
  methods: {
    plusOne() {
      this.counter += 1;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

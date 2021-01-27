<template>
  <div id="app">
    <AppTitle msg="Silly App"/>
    <CounterResult :counter="counter" />
    <ControlButtons @increaseOne="plusOne" @decreaseOne="minusOne"/>
  </div>
</template>

<script>
import AppTitle from './components/AppTitle.vue'
import CounterResult from './components/CounterResult';
import ControlButtons from './components/ControlButtons';

export default {
  name: 'App',
  components: {
    AppTitle,
    CounterResult,
    ControlButtons,
  },
  data: function() {
    return {
      counter: 0
    }
  },
  methods: {
    plusOne() {
      this.counter += 1;
    },

    minusOne() {
      this.counter -= 1;
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

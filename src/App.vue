<template>
  <div id="app">
    <date-range-picker
        @apply="onDateChange"
        opens="left"
    >
    </date-range-picker>
  </div>
</template>

<script>
import DateRangePicker from './components/DateRangePicker.vue'

export default {
  name: 'app',
  components: {DateRangePicker},
  data () {
    return {
      start: null,
      end: null
    }
  },
  methods: {
    onDateChange (start, end) {
      this.start = start
      this.end = end
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

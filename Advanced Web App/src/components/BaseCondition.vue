

<template>
  <div id="app">
    <h1>Temperature Converter</h1>
    <div>
      <label for="celsius">Celsius:</label>
      <input type="number" v-model="celsius" @input="convertTemperature" />
    </div>
    <div>
      <label for="fahrenheit">Fahrenheit:</label>
      <input type="number" v-model="fahrenheit" @input="convertTemperature" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      celsius: 0,
      fahrenheit: 32,
    };
  },
  methods: {
    convertTemperature() {
      // Convert Celsius to Fahrenheit
      this.fahrenheit = (this.celsius * 9/5) + 32;
      
      // Convert Fahrenheit to Celsius
      // this.celsius = (this.fahrenheit - 32) * 5/9;
    },
  },
};
</script>

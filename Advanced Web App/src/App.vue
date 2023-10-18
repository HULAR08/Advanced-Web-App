
<template>
  <div>
    <h1>Temperature Converter</h1>

    <div>
      <label for="celsius">Celsius:</label>
      <input type="number" id="celsius" v-model="celsius" @input="convertToFahrenheit">
    </div>

    <div>
      <label for="fahrenheit">Fahrenheit:</label>
      <input type="number" id="fahrenheit" v-model="fahrenheit" @input="convertToCelsius">
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
    convertToFahrenheit() {
     
      this.fahrenheit = this.celsius * 9/5 + 32;
    },
    convertToCelsius() {

      this.celsius = (this.fahrenheit - 32) * 5/9;
    },
  },
};
</script>


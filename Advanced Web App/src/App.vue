

<template>
  <div id="app">
    <BaseCondition :showComponent="true" />
    <BaseLoop />
  </div>
</template>

<script>
import BaseCondition from './components/basecondition.vue';
import BaseLoop from './components/baseloop.vue';

export default {
  components: {
    BaseCondition,
    BaseLoop,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: 'Helvetica Neue', sans-serif;
}
</style>
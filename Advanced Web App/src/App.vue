

<template>
  <div id="app">
    <BaseCondition :showComponent="true" />
    <BaseLoop />
    <flexbox />
  </div>
</template>

<script>
import BaseCondition from './components/basecondition.vue';
import BaseLoop from './components/baseloop.vue';
import flexbox from './components/flexbox.vue';
export default {
  components: {
    BaseCondition,
    BaseLoop,
    flexbox,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: 'Helvetica Neue', sans-serif;
}
</style>


<template>
  <div id="app">
    <TestComponent />
    <PackageJsonDisplay />
  </div>
</template>

<script>
import TestComponent from './components/TestComponent.vue';
import PackageJsonDisplay from './components/PackageJsonDisplay.vue';

export default {
  name: 'App',
  components: {
    TestComponent,
    PackageJsonDisplay
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>

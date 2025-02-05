<template>
    <div class="test-component">
      <img alt="Yippee" src="../assets/yippee.gif">
      <HelloWorld :msg="message" />
    </div>
  </template>
  
  <script>
  import HelloWorld from './HelloWorld.vue';
  
  export default {
    name: 'TestComponent',
    components: {
      HelloWorld,
    },
    data() {
      return {
        message: "The test of the testing has worked!"
      };
    },
  };
  </script>
  
  <style scoped>
  .test-component {
    text-align: center;
    margin-top: 20px;
  }
  
  .test-component img {
    width: 200px;
    height: auto;
  }
  
  .test-component p {
    font-size: 20px;
    color: #4CAF50;
    font-weight: bold;
  }
  </style>
  
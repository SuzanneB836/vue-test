<!-- src/components/PackageJsonDisplay.vue -->
<template>
    <div>
      <h1>Package.json Content</h1>
      <pre>{{ packageData }}</pre>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        packageData: ''
      };
    },
    mounted() {
      // Fetch the package.json from the public folder
      fetch('./package.json')
        .then(response => response.json())
        .then(data => {
          this.packageData = JSON.stringify(data, null, 2);
        })
        .catch(error => {
          console.error('Error fetching package.json:', error);
        });
    }
  };
  </script>
  
  <style scoped>
  /* You can add styles here to format the content if needed */
  pre {
    background-color: #f4f4f4;
    padding: 1rem;
    border-radius: 5px;
  }
  </style>
  
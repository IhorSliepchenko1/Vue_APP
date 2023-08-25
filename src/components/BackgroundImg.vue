<template>
    <img :src="src" :alt="alt" />
  </template>
  
  <script>
  export default {
    name: 'BackgroundImg',
    props: {
      src: String,
      alt: String
    }
  };
  </script>
  
  
  
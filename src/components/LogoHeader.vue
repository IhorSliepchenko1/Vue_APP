<template>
    <div class="logo">
      <LogoIcon />
      PNFT Market
    </div>
  </template>
  
  <script>
  import LogoIcon from "./icons/LogoIcon.vue";
  
  export default {
    components: {
      LogoIcon
    }
  };
  </script>
  
  <style scoped>
  .logo {
    display: flex;
    align-items: center;
    gap: 12px;
    font-family: Inter;
    font-size: 18px;
    font-weight: 600;
    color: #344054;
  }
  </style>
  
<template>
    <div class="card">
      <img :src="card.image" alt="Card image" />
      <div class="card-details">
        <h3>{{ card.label }}</h3>
        <p><strong>Name:</strong> {{ card.name }}</p>
        <p><strong></strong> {{ card.address }}</p>
       
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      card: {
        type: Object,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  body {
    background-color: #f76d24;
    margin: 0%;
    padding: 0%;
    
  }
  .card {
    border: 1px solid #f76d24;
    border-radius: 8px;
    padding: 16px;
    margin: 10px;
    width: 100%;
    background-color: #fff;
    color: black;
    margin-left: 40px;
    text-align: center;
    
  }
  
  .card img {
    max-width: 100%;
    border-radius: 4px;
  }
  
  .card-details {
    margin-top: 8px;
  }
  </style>
  
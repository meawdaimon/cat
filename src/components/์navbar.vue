<template>
    <nav class="navbar">
      <div class="navbar-left">
        <img src="@/assets/logo.png" alt="Logo" class="logo" />
      </div>
      <div class="navbar-right">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Product</a></li>
          <li><a href="#">About</a></li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
  };
  </script>
  
  <style scoped>
  .navbar {
    background-color: #333;
    color: white;
    padding: 15px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo {
    width: 50px;
    height: auto;
  }
  
  .navbar-right ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    gap: 20px;
  }
  
  .navbar-right ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
    padding: 5px 10px;
    transition: background-color 0.3s;
  }
  
  .navbar-right ul li a:hover {
    background-color: #555;
    border-radius: 5px;
  }
  </style>
  
<template>


  <div id="app" class="app-container">
    <Navbar />

    <h1>แมว 12 สายพันธุ์แมวน่าเลี้ยง </h1><br>
    

 
    <div class="card-container">
      <Card v-for="(card, index) in cards" :key="index" :card="card" />
    </div>
  </div>
</template>

<script>
import Card from './components/card.vue';
import jsonData from './components/vue.json'; // Import JSON data
import Navbar from './components/์navbar.vue'; // Import the Navbar component

export default {
  name: 'App',
  components: {
    Navbar,
    Card,
  },
  data() {
    return {
      cards: jsonData,
    };
  },
};
</script>

<style>
body {
  background-color: antiquewhite;
  margin-top: 5%;
  padding: 0;
}
h1 {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
  color: black;
  text-align: center;
  margin-top: 5%;
  margin-left: 50%;
  width: 250%;
  margin-bottom: 3%;
}

.app-container {
  padding-top: 100px; /* Ensure enough space below the navbar */
  color: white;

}

/* Card Container */
.card-container {
  display: flex;
  flex-wrap: wrap; /* อนุญาตให้การ์ดขึ้นบรรทัดใหม่ */
  justify-content: center; /* จัดการ์ดให้อยู่กลาง */
  gap: 20px; /* เพิ่มช่องว่างระหว่างการ์ด */
  padding: 10px;
  width: 350%;
}

.card-container .card {
  flex: 0 0 calc(30% - 20px); /* 3 การ์ดต่อแถว */
  box-sizing: border-box;
  margin-bottom: 20px; /* เพิ่มช่องว่างด้านล่างของการ์ด */
  min-width: 250px; /* ขนาดขั้นต่ำของการ์ด */
  max-width: 300px; /* ขนาดสูงสุดของการ์ด */
  background-color: white;
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1); /* เพิ่มเงาเพื่อให้การ์ดดูมีมิติ */
  transition: transform 0.3s ease;
}

.card-container .card:hover {
  transform: scale(1.05); /* ขยายการ์ดเล็กน้อยเมื่อ hover */
}


</style>

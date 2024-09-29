<template>
    <div>
      <h1 v-if="isshow">Hiển thị phần tử</h1>
      <h1 v-else>Ẩn phần tử</h1>
      <button @click="handleToggle">Toggle</button>
  
      
      <h1 v-if="age >= 18">Đủ tuổi thi</h1>
      <h1 v-else>Chưa đủ tuổi thi</h1>
      <h1>Tuổi : {{age }}</h1>
      <button @click="handleIncreaseAge">Tăng tuổi</button>
      <button v-on:click="handleDecreaseAge">Giảm tuổi</button>
     
      <h1 v-if="role === 'admin'">Quyền admin</h1>
      <h1 v-else-if="role === 'user'">Quyền user</h1>
      <h1 v-else-if="role === 'edit'">Quyền edit</h1>
      <h1 v-else>Quyền other</h1>
      
      <h1 v-show="isShowForm">From Content</h1>
    </div>
  </template>
  
  <script setup>
    import { ref } from "vue";
  
    const isshow = ref(true);
    const age = ref(0);
    const role = ref("creator");
    const isShowForm = ref(false);
    const handleToggle = () => {
      isshow.value = !isshow.value;
    };
  
    const handleIncreaseAge = () =>{
        age.value++;
    };
    const handleDecreaseAge = () =>{
        age.value--;
    };
    
  </script>
  
  <style>

  </style>
  
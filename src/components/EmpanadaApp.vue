<template>
    <div id="app">
      <h1>Empanada Tracker</h1>
      <input v-model="newEmpanada" placeholder="Nuevo sabor de empanada" />
      <button @click="addEmpanada">Agregar Empanada</button>
      <ul>
        <li v-for="(empanada, index) in empanadas" :key="index">
          {{ empanada.name }}: {{ empanada.quantity }}
          <button @click="increment(index)">+</button>
          <button @click="decrement(index)">-</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'EmpanadaApp',
    data() {
      return {
        newEmpanada: '',
        empanadas: []
      };
    },
    methods: {
      addEmpanada() {
        if (this.newEmpanada.trim() !== '') {
          this.empanadas.push({ name: this.newEmpanada, quantity: 0 });
          this.newEmpanada = '';
        }
      },
      increment(index) {
        this.empanadas[index].quantity++;
      },
      decrement(index) {
        if (this.empanadas[index].quantity > 0) {
          this.empanadas[index].quantity--;
        }
      }
    }
  };
  </script>
  
  <style scoped>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
  button {
    margin-left: 10px;
  }
  </style>
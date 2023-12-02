<script setup>
import Calculadora_script from './components/Calculadora_script.vue';

</script>

<template>
  <Calculadora_script />
</template>

<style scoped>
    #app {
  font-family: 'Arial', sans-serif;
}

.container {
  background-color: #f3f3f3;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}

input,
select {
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 4px;
}


input[disabled] {
  background-color: #eee;
}

.result {
  font-size: 1.2em;
  font-weight: bold;
  color: #333;
  margin-top: 10px;
}
</style>

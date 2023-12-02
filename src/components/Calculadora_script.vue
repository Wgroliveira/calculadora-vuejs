<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      operation: 'add',
    };
  },
  computed: {
    calculateResult() {
      const num1 = parseFloat(this.num1);
      const num2 = parseFloat(this.num2);

      switch (this.operation) {
        case 'add':
          return num1 + num2;
        case 'subtract':
          return num1 - num2;
        case 'multiply':
          return num1 * num2;
        case 'divide':
          return num1 / num2;
        default:
          return 0;
      }
    },
  },
};
</script>

<template>
    <div id="app" class="container mt-5">
        <div class="row">
            <div class="col-md-4 offset-md-4">
                <h2 class="mb-4">Calculadora Aritmética</h2>
                
                    <div class="form-group mb-3">
                        <label for="num1">Número 1:</label>
                        <input v-model="num1" type="number" class="form-control">
                    </div>

                    <div class="form-group mb-3">
                        <label for="num2">Número 2:</label>
                        <input v-model="num2" type="number" class="form-control">
                    </div>

                    <div class="form-group mb-3">
                        <label for="operation" class="select-label">Operação:</label>
                        <select v-model="operation" class="form-control">
                            <option value="add">+</option>
                            <option value="subtract">-</option>
                            <option value="multiply">*</option>
                            <option value="divide">/</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label for="result">Resultado:</label>
                        <input :value="calculateResult" type="text" class="form-control" disabled>
                    </div>
            </div>
        </div>
    </div>
</template>

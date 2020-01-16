<template>
  <img src="./logo.png">
  <h1>Hello Vue 3!</h1>
  <dx-button text="click"></dx-button>
  <button @click="inc">Clicked {{ count }} times.</button>
</template>

<script>
import { ref } from 'vue'
import { DxButton } from 'devextreme-vue/button';

export default {
  components: {
    DxButton
  },
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
}
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>

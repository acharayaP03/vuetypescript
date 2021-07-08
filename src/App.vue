<template>
  <h1>Hello {{ name }} - {{ age }}</h1>
  <button @click="changeName('Trishten Ac ')">change name</button>
  <button @click="changeAge(39)">Change age</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  components: {},
  data() {
    return {
      name: 'link',
      age: 38 as number | string,
    }
  },
  methods: {
    changeName(name: string) {
      return (this.name = name)
    },
    changeAge(age: number | string) {
      return (this.age = age)
    },
  },
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap');
body {
  font-family: 'Open Sans';
  background-color: #ece6d9;
}
h1 {
  margin: 0 auto;
  text-align: center;
}
</style>

<template>
  <h1>Hello {{ name }} - {{ age }}</h1>
  <button @click="changeName('Trishten Ac ')">change name</button>
  <button @click="changeAge(39)">Change age</button>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    const state = reactive({
      name: 'Link',
      age: 38 as number | string,
    })

    /**
     * if we happened to use ref, then when declaring age, we need to infer type as below
     * const age = ref<number | string>(38)
     * because ref return a refrence of an object, hence we cannot infer types after as we did above on reactive
     */
    function changeName(name: string) {
      return (state.name = name)
    }
    function changeAge(age: number | string) {
      return (state.age = age)
    }

    return { ...toRefs(state), changeName, changeAge }
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

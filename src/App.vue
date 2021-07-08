<template> 
<h1>Hello Type script</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
  name: 'App',
  components: {
  }
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap');
body{
    font-family: 'Open Sans';
    background-color: #ece6d9;
}
h1{
  margin: 0 auto;
  text-align: center;
}
</style>

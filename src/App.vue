<template>
  <header>
    <div class="order">
      <button @click="handleClick('title')">Order By Title</button>
      <button @click="handleClick('location')">Order By Location</button>
      <button @click="handleClick('salary')">Order By  Salary</button>
    </div>
  </header>
  <job-list :jobs="jobs" :order="order"></job-list>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import JobList from '@/components/JobList.vue'
import Jobs from './types/Job'
import OrderTerm from '@/types/OrderTerm'

export default defineComponent({
  name: 'App',
  components: {
    JobList,
  },
  setup() {
    const jobs = ref<Jobs[]>([
      {
        title: 'Farm Worker',
        location: 'Lon lon ranch',
        salary: 30000,
        id: '1',
      },
      {
        title: 'quarrman',
        location: 'death mountain',
        salary: 50000,
        id: '2',
      },
      {
        title: 'Flute player',
        location: 'the lost wood',
        salary: 35000,
        id: '3',
      },
      {
        title: 'Fisher man',
        location: 'Lake hylia',
        salary: 21000,
        id: '12',
      },
      {
        title: 'prision guard',
        location: 'gerudo valley',
        salary: 32000,
        id: '5',
      },
    ])

    const order = ref<OrderTerm>('title')

    function handleClick(term: OrderTerm) {
      order.value = term
    }

    return { jobs, order, handleClick }
  },
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap');
body {
  font-family: 'Open Sans';
  background-color: #ece6d9;
}
header {
  text-align: center;
}
header .order {
  margin-top: 20px;
}
button {
  margin: 0 10px;
  color: #1195c9;
  border: 3px solid #1195c9;
  background: #d5f0ff;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
}
</style>

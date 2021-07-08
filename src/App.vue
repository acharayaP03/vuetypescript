<template>
  <job-list :jobs="jobs"></job-list>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import JobList from '@/components/JobList.vue'
import Jobs from './types/Job'

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

    return { jobs }
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

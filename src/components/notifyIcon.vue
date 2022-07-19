<template>
  <div v-for="item in data2" :key="item.id">
    <div class="w-8 h-5 bg-red rounded-3xl flex justify-center item-center ">
          {{item.notifyMenu}}
    </div>
  </div>

</template>

<script>
import jsonData2 from '/src/data2.json'


export default {
  data() {
    return{
      statues: [],
      data2: jsonData2


    }
  },

  name: 'kysKys',
  props: {
    msg: String
  }
}

</script>



<style>

</style>
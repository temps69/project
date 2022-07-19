<div v-for="item in data" :key="item.id">
<div  v-for="item2 in data2" :key="item2.id">
  <object>
    <img alt="mailobr" src="../assets/forum_FILL0_wght400_GRAD0_opsz48.png"
         class="w-8">
    <div  @click="item2.notifyMenu--"
          class=" text-sm font-bold p-3 cursor-pointer flex right-2">
      {{item.title}} {{item.id}} - {{item.name}} ¤ {{item.time}}
    </div>
    <div class="text-lg p-1">
      {{item.content}}
    </div>
  </object>
</div>
</div>




<div v-for="item in data" :key="item.id">

<div v-for="item2 in data2" :key="item2.id">
  <div @click="item2.notifyMenu--"
       class=" text-sm font-bold p-3 cursor-pointer flex right-2">
    <img alt="mailobr" src="../assets/forum_FILL0_wght400_GRAD0_opsz48.png"
         class="w-8">
    {{item.title}} {{item.id}} - {{item.name}} ¤ {{item.time}}
  </div>

</div>


<div class="text-lg p-1">

  {{item.content}}

</div>
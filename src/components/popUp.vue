<template>



  <div class="popup">
    <div class="popupInner  absolute top-20 overflow-y-scroll">

      <table v-for="item2 in data2" :key="item2.id"
             class="pepa text-l  h-16">
      <tr>

        <td class="p-2 cursor-pointer font-bold">Přehled {{item2.summary}}</td>
        <td class="p-2 cursor-pointer font-bold">Příležitosti {{item2.opportunities}}</td>
        <td class="p-2 cursor-pointer font-bold">Smlouvy {{item2.contracts}}</td>
        <td class="p-2 cursor-pointer font-bold">Diskuze {{item2.discussion}}</td>
        <td class="p-2 cursor-pointer font-bold">Přepuštění {{item2.abandonment}}</td>
        <td class="p-2 cursor-pointer font-bold">Rezervace {{item2.reservation}}</td>
        <td>

        </td>

      </tr>
      </table>



      <slot/>
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

      </div>



    </div>
  </div>

</template>

<script>
import jsonData from '/src/data.json'
import jsonData2 from '/src/data2.json'
import notifyIcon from "@/components/notifyIcon";

export default {
  data() {
    return{
      statues: [],
      data: jsonData,
      data2: jsonData2,
      notifyIcon


    }
  },

  name: 'PopUp',
  components: {

 }
}

</script>



<style>
.popupInner{
  background: white;
  width: 645px;
  height: 500px;
  right: 100px;
  box-shadow: 0px 4px 16px #00000026;

}

</style>
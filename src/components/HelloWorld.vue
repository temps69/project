<template>
 <div class="bg-green h-20 flex justify-center p-3">

    <pop-up v-if="popupTriggers.buttonTrigger">

    </pop-up>



   <div class="absolute right-96 w-12 h-10 cursor-pointer">
     <img alt="mailobr" src="../assets/calendar_month_FILL0_wght400_GRAD0_opsz48.png"
          class="w-10">
   </div>

   <div class="absolute right-64 w-12 h-10 cursor-pointer">
     <img alt="mailobr" src="../assets/notifications_FILL0_wght400_GRAD0_opsz48.png"
          class="w-10">
   </div>

   <div class="absolute right-32 w-15 h-15 cursor-pointer"
        @click="() => TogglePopup('buttonTrigger')">
     <img alt="mailobr" src="../assets/mail_FILL0_wght400_GRAD0_opsz48.png"
          class="w-10">
     <notify-icon></notify-icon>
   </div>



   <div class="absolute right-5 w-12 h-10 cursor-pointer">
     <img alt="mailobr" src="../assets/timer_FILL0_wght400_GRAD0_opsz48.png"
          class="w-10">
   </div>

   <div class=" bg-blue w-10 h-10 left-96">

   </div>
 </div>

</template>

<script>
import PopUp from "@/components/popUp";
import {ref} from "vue";
import notifyIcon from "@/components/notifyIcon";

export default {



  setup () {
    const popupTriggers = ref({
      buttonTrigger: false,
      timeTrigger: false
    });

    const TogglePopup = (trigger) => {
      popupTriggers.value[trigger] = !popupTriggers.value[trigger]
    }

    return{
      PopUp,
      popupTriggers,
      TogglePopup,
      notifyIcon

    }
  },

  name: 'HelloWorld',
  components: {
   PopUp,
    notifyIcon

  }
}
</script>


<style>

</style>

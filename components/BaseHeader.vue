<template>
  <div>
    <!--Header-->
    <div class="w-full h-20 px-8 text-center text-white bg-black">
      <div class="flex">
        <span class="w-16 h-16">
            <img @click="backEvent" class="mt-3 cursor-pointer grow" src="../static/Principales/BotónAtrás.png" alt="">
        </span>
        <span class="flex justify-center w-full">
            <img class="py-2 mt-2 cursor-pointer grow" src="../static/Principales/Logo.png" alt="">
        </span>
        <span class="w-16 h-16">
              <img @click="homeEvent" class="mt-3 cursor-pointer grow" src="../static/Principales/BotónHome.png" alt="">
        </span>
      </div>
    </div>
<!--Header End-->
  </div>
</template>

<script>

import Principales from "../Principales/Principales.vue";

export default {
  coomponents:{
    Principales
  },
  data(){
    return{
      componentKey: 0,
    }
  },
  methods:{
    backEvent(event){
      this.$emit('back-event', event)
    },

    homeEvent(event){
      this.$emit('pass-event', Principales)

    },
  }
};
</script>

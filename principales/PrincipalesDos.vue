<template>
<section>
    <div  class="flex flex-col w-full ">
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
              <img @click="passEvent('Principales')" class="mt-3 cursor-pointer grow" src="../static/Principales/BotónHome.png" alt="">
        </span>
      </div>
    </div>
<!--Header End-->
                <span class="flex flex-col w-full ">

                    <img class="w-1/2 mx-auto mt-24" src="../static/Principales/principalDos/titulo.png" alt="">
                </span>
                <span class="absolute z-10 flex justify-center w-full mt-80">
                    <div v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1.25}]" class="top-0 flex justify-center w-1/2 opacity-80 hover:opacity-100">
                        <img @click="toggle = !toggle" class="cursor-pointer grow h-3/5" src="../static/Principales/principalDos/menos18.png" alt="">
                    </div>
                    <div v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1.5}]" class="top-0 flex justify-center w-1/2 opacity-80 hover:opacity-100">
                        <img @click="passEvent('Formulario')" class="cursor-pointer grow h-3/5" src="../static/Principales/principalDos/mas18.png" alt="">
                    </div>
                    <img v-if="toggle == true" @click="toggle = !toggle" class="absolute cursor-pointer" src="../static/Principales/principalDos/Popoup.png" alt="">
                </span>


    </div>
</section>
</template>

<script>
import Principales from '../principales/Principales.vue'
import BaseHeader from '../components/BaseHeader.vue'

export default {
  components: {
    BaseHeader,
  },
  data() {
    return {
      toggle: false,
    }
  },
  methods: {
    passEvent(event)
    {

      this.$emit('pass-event', event)
    },
    backEvent(event)
    {

      this.$emit('pass-event', Principales)
    },

  }
}
</script>


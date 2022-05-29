<template>

<section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <div  class="flex w-full ">
        <span class="flex justify-center w-full ">

            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="relative transform scale-75"  src="../static/Infografias/BeefeaterBlackberry/contenido.png" alt="">
            <base-header class="absolute w-full" @pass-event="passEvent" @back-event="backEvent"></base-header></spa>
        </span>
      <span v-gsap.fromTo="[{ x: 700 }, { x: 0,  duration: 1.25}]" class="absolute flex justify-end w-4/5 bottom-40 ">
      <img  @click="passEvent('CoctelBlackBerry')" class="absolute cursor-pointer grow" src="../static/Infografias/BeefeaterBlackberry/MIXOLOGÍA.png" alt="">
      </span>
    </div>
    </section>
</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import CoctelBlackBerry from "../Cocteles/CoctelBlackBerry.vue";
import BeefEater from "../Principales/BeefEater.vue";
import bgImg from "../static/Infografias/BeefeaterBlackberry/fondo.png"

export default {
  components: {
    BaseHeader,
    CoctelBlackBerry,
    BeefEater,
    bgImg
  },
  data() {
    return {
      image: { backgroundImage: `url(${bgImg})` },
    };
  },
  methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event )
    },
    backEvent(event)
    {
      this.$emit('pass-event', BeefEater)
    },
  }
};
</script>

<template>

<section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <div  class="flex w-full ">
        <span class="flex justify-center w-full ">

            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="relative transform scale-75"  src="../static/Infografias/MonkeySloeGin/contenido.png" alt="">
            <base-header class="absolute w-full" @pass-event="passEvent" @back-event="backEvent"></base-header></spa>
        </span>
      <span v-gsap.fromTo="[{ x: 700 }, { x: 0,  duration: 1.25}]" class="absolute flex justify-end w-4/5 bottom-40 ">
      <img  @click="passEvent('CoctelMonkeySloeGin')" class="absolute cursor-pointer grow" src="../static/Infografias/MonkeySloeGin/MIXOLOGÍA.png" alt="">
      </span>
    </div>
    </section>
</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import CoctelMonkeySloeGin from "../Cocteles/CoctelMonkeySloeGin.vue";
import Monkey from "../Principales/Monkey.vue";
import bgImg from "../static/Infografias/MonkeySloeGin/fondo.png"

export default {
  components: {
    BaseHeader,
    CoctelMonkeySloeGin,
    Monkey,
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
      this.$emit('pass-event', Monkey)
    },
  }
};
</script>

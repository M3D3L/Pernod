<template>
<span>
<base-header @pass-event="passEvent" @back-event="backEvent"></base-header>
<section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <div  class="relative flex w-full">
        <span class="relative flex justify-center w-full">
            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="transform scale-75"  src="../static/Infografias/Mumm/contenido.png" alt="">
        </span>
      <span v-gsap.fromTo="[{ x: 700 }, { x: 0,  duration: 1.25}]" class="absolute flex justify-end w-4/5 bottom-40 ">
      <img  @click="passEvent('CoctelHavanaClub7')" class="absolute cursor-pointer grow" src="../static/Infografias/Mumm/MIXOLOGÍA.png" alt="">
      </span>
    </div>
    </section>
</span>

</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import CoctelHavanaClub7 from "../Cocteles/CoctelHavanaClub7.vue";
import PrincipalesTres from "../Principales/PrincipalesTres.vue";
import bgImg from "../static/Infografias/Mumm/fondo.png"
export default {
  components: {
    BaseHeader,
    CoctelHavanaClub7,
    PrincipalesTres,
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
      this.$emit('pass-event', PrincipalesTres)
    },
  }
};
</script>

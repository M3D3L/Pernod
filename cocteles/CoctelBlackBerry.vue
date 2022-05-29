<template>
    <section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <base-header class="absolute w-full" @pass-event="passEvent" @back-event="backEvent"></base-header>
    <div  class="flex justify-center w-full">
        <span class="flex justify-center w-full mt-20">
            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="my-auto transform"  src="../static/Cocteles/CoctelBlackBerry/contenido.png" alt="">
            <span class="flex justify-end">
                <span v-gsap.fromTo="[{ x: 700, scale: .75 }, { x: 0, scale:1, duration: 1.25}]" class="absolute bottom-10">
                    <img  class="pr-20 cursor-pointer grow" src="../static/Cocteles/CoctelBlackBerry/MIXOLOGÍA.png" alt="">
                </span>
            </span>

        </span>
        <div v-gsap.fromTo="[{ x: -700 }, { x: 0,  duration: 1.25}]" class="absolute w-1/2 mb-16 bottom-20 left-10 bg-red-50 h-1/2">
            <iframe class="object-cover w-full h-full" src="https://www.youtube.com/embed/OhyQRljsp2w?autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
    </section>
</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import bgImg from "../static/Cocteles/CoctelBlackBerry/fondo.png";
import BeefEaterBlackberry from "../Infografias/BeefEaterBlackberry.vue";

export default {
  components:{
    BaseHeader,
    bgImg,
    BeefEaterBlackberry
  },
  data() {
    return {
      image: { backgroundImage: `url(${bgImg})` },
    };
  },
  methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event)
    },
    backEvent(event)
    {
      this.$emit('pass-event', BeefEaterBlackberry)
    },
  }
};
</script>

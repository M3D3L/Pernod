<template>
    <section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <base-header class="absolute w-full" @pass-event="passEvent" @back-event="backEvent"></base-header>
    <div  class="flex justify-center w-full">
        <span class="flex justify-center w-full mt-10">
            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="my-auto transform scale-75"  src="../static/Cocteles/CoctelMonkeyDryGin/contenido.png" alt="">
            <span class="flex justify-end">
                <span v-gsap.fromTo="[{ x: 700, scale: .75 }, { x: 0, scale:1, duration: 1.25}]" class="absolute bottom-20">
                    <img  class="pr-20 cursor-pointer grow" src="../static/Cocteles/CoctelMonkeyDryGin/MIXOLOGÍA.png" alt="">
                </span>
            </span>

        </span>
        <div v-gsap.fromTo="[{ x: -700 }, { x: 0,  duration: 1.25}]" class="absolute w-1/2 pl-12 mb-16 bottom-20 left-10 h-1/2">
            <iframe class="object-cover w-full h-full " src="https://www.youtube.com/embed/OhyQRljsp2w?autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
    </section>
</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import bgImg from "../static/Cocteles/CoctelMonkeyDryGin/fondo.png";
import Monkey from "../Principales/Monkey.vue";

export default {
  components:{
    BaseHeader,
    Monkey
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
      this.$emit('pass-event', Monkey)
    },
  }
};
</script>

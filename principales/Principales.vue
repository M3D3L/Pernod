
<template>
<section  class="flex justify-center w-full h-screen">
  <span v-gsap.fromTo="[{ y: -700 }, { y: 0, duration: 1}]"  class="absolute bottom-0 z-0 ">
    <img   src="../static/Principales/principalUno/botellas.png" alt="">
  </span>
  <span class="w-full z-90">
    <span class="flex flex-col w-full">
      <div class="flex justify-center w-full">
        <img class="h-24 py-2 mt-16 cursor-pointer" src="../static/Principales/Logo.png" alt="">
      </div>
    </span>
    <div>
      <span class="flex justify-center w-full mt-16 h-36">
        <h1 class="flex justify-center w-4/5 rounded-full cursor-pointer h-36 z-100">
          <img class="absolute mt-10 ml-2 opacity-20" src="../static/Principales/principalUno/cta.png" alt="">
          <img class="absolute mt-10" src="../static/Principales/principalUno/cta.png" alt="">
        </h1>
      </span>
      <span v-gsap.fromTo="[{ y: 100, scale: .75 }, { y: 0, scale:1, duration: 1}]"  class="z-10 flex justify-center transform animate-pulse">
        <img @click="passEvent" class="cursor-pointer grow" src="../static/Principales/principalUno/boton.png" alt="">

      </span>
    </div>
  </span>
</section>

</template>

<script>
import PrincipalesDos from '../principales/PrincipalesDos.vue'

export default {
  components: {
    PrincipalesDos,
  },
  methods: {
    passEvent()
    {
      this.$emit('pass-event', PrincipalesDos)
    },
  }
}

</script>

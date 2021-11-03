
<template>
<section >
        <span class="flex flex-col w-full">
          <base-header class="w-full h-20 bg-black " @back-event="backEvent" @pass-event="passEvent"></base-header>
                <img class="w-1/2 mx-auto" src="../static/Principales/formualrio/TítulO.png" alt="">

            <div class="flex justify-center mt-4">

                <span class="flex flex-col w-3/5 ml-48 ">
                  <span class="flex flex-row w-full">
                    <h2 class="flex h-16 text-3xl font-bold text-white w-96 neon-text">Nombre Completo</h2>
                    <input type="flex text-3xl font-bold text-white w-96">
                  </span>
                    <div class="flex flex-row">
                      <h2 class="flex flex-row mt-8 text-3xl font-bold text-white w-96 neon-text">Fecha De Nacimiento</h2>
                      <span class="flex flex-row w-1/2 space-x-4">

                      <select class="w-1/3 h-16 mt-8 text-center bg-purple-500 neon-text bg-opacity-20 ">
                        <option value='día'>Día</option>
                        <option value='1'>1</option>
                        <option value='2'>2</option>
                        <option value='3'>3</option>
                        <option value='4'>4</option>
                        <option value='5'>5</option>
                        <option value='6'>6</option>
                        <option value='7'>7</option>
                        <option value='8'>8</option>
                        <option value='9'>9</option>
                        <option value='10'>10</option>
                        <option value='11'>11</option>
                        <option value='12'>12</option>
                        <option value='13'>13</option>
                        <option value='14'>14</option>
                        <option value='15'>15</option>
                        <option value='16'>16</option>
                        <option value='17'>17</option>
                        <option value='18'>18</option>
                        <option value='19'>19</option>
                        <option value='20'>20</option>
                        <option value='21'>21</option>
                        <option value='22'>22</option>
                        <option value='23'>23</option>
                        <option value='24'>24</option>
                        <option value='25'>25</option>
                        <option value='26'>26</option>
                        <option value='27'>27</option>
                        <option value='28'>28</option>
                        <option value='29'>29</option>
                        <option value='30'>30</option>
                        <option value='31'>31</option>
                      </select>
                      <select class="w-1/3 h-16 mt-8 text-center bg-purple-500 bg-opacity-20 neon-text">
                        <option value='1'>Mes</option>
                        <option value='2'>Enero</option>
                        <option value='3'>Febrero</option>
                        <option value='4'>Marzo</option>
                        <option value='2'>Abril</option>
                        <option value='3'>Mayo</option>
                        <option value='4'>Junio</option>
                        <option value='4'>Julio</option>
                        <option value='2'>Agosto</option>
                        <option value='3'>Septiembre</option>
                        <option value='4'>Octubre</option>
                        <option value='2'>Noviembre</option>
                        <option value='3'>Diciembre</option>
                      </select>
                      <select class="w-1/3 h-16 mt-8 text-center bg-purple-500 neon-text bg-opacity-20 ">
                        <option value='1'>Año</option>
                        <option value='2'>option2</option>
                        <option value='3'>option3</option>
                        <option value='4'>option3</option>
                      </select>
                    </span>
                    </div>

                    <span class="flex flex-row mt-8 ">
                      <h2 class="flex flex-row text-3xl font-bold text-white w-96 neon-text ">Correo Electrónico</h2>
                      <input type="flex flex-row text-3xl font-bold text-white w-96  neon-text">
                    </span>
                    <span class="flex flex-row">
                      <h2 class="flex flex-row mt-8 text-3xl font-bold text-white w-96 neon-text ">Bebida Favorita</h2>
                      <select class="w-1/2 mt-8 bg-purple-500 neon-text bg-opacity-20">
                        <option value=''>--Seleccione Una Opción-- </option>
                        <option value='AbsolutBlue'>Absolut Blue</option>
                        <option value='AbsolutExtrakt'>Absolut Extrakt</option>
                        <option value='AbsolutSabores'>Absolut Sabores</option>
                        <option value='Altos'>Altos</option>
                        <option value='Ballantines'>Ballantines</option>
                        <option value='BeefEaterBlackBerry'>BeefEater BlackBerry</option>
                        <option value='BeefEaterLondon'>BeefEater London</option>
                        <option value='BeefEaterPink'>BeefEater Pink</option>
                        <option value='AbsolutBlue'>Absolut Blue</option>
                        <option value='Chivas12'>Chivas 12</option>
                        <option value='ChivasExtra'>Chivas Extra</option>
                        <option value='ChivasTequila'>Chivas Tequila</option>
                        <option value='HavanaClub7'>HavanaClub7</option>
                        <option value='Jameson'>Jameson</option>
                        <option value='MartellBlueSwift'>Martell Blue Swift</option>
                        <option value='MartellVSOP'>Martell VSOP</option>
                        <option value='MonkeyDryGin'>Monkey Dry Gin</option>
                        <option value='MonkeySloeGin'>Monkey Sloe Gin</option>
                        <option value='Mumm'>Mumm</option>
                        <option value='TheGlenLivet'>The Glen Livet</option>
                      </select>
                    </span>

                </span>
            </div>

        </span>
        <span class="flex justify-center w-full mt-8 space-x-4">
          <input class="w-16 h-16 mt-12" type="checkbox" id="vehicle2" name="vehicle2" value="Car">
          <p class="w-1/2 px-32 mx-auto mt-8 text-xl text-white">Al dar click en "enviar" autorizo a <span class="font-bold">Pernod Ricard México</span> a utilizar mis datos para servicios y promociones.
        Si quieres mayor información puedes consultar nuestro <span class="font-bold">Aviso de Privacidad</span> </p>

          <img @click="passEvent('PrincipalesTres')" class="mt-2 cursor-pointer grow" src="../static/Principales/formualrio/ENVIAR.png" alt="">
        </span>

</section>

</template>

<script>

import PrincipalesDos from '../Principales/PrincipalesDos.vue'
import BaseHeader from '../components/BaseHeader.vue'

export default {
  components: {
    BaseHeader,
  },

  methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event)
    },
    backEvent(event)
    {
      this.$emit('pass-event', PrincipalesDos)
    },

  }
}
</script>

<style>
  .w-cstm{
  width: 100%;
  }
</style>


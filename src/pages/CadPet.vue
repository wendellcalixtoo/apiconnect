<template>
  <q-page class="row flex justify-center bg-pink-1">
    <q-card class="q-pa-md my-card bg-grey-2 text-black shadow-1 col-10">
        <div class="q-pa-lx">
    <q-carousel

      animated
      v-model="slide"
      navigation
      infinite
      autoplay
      transition-prev="slide-right"
      transition-next="slide-left"
    >
      <q-carousel-slide :name="1" img-src="https://wallpaperaccess.com/full/497595.jpg" />
      <q-carousel-slide :name="2" img-src="https://www.wallpaperup.com/uploads/wallpapers/2014/04/01/318600/97d2f1bbbfc8d39b19fbbf50483fc440.jpg" />
      <q-carousel-slide :name="3" img-src="https://i.ytimg.com/vi/69Zo05WeIF0/maxresdefault.jpg" />
      <q-carousel-slide :name="4" img-src="https://wallpapersite.com/images/pages/pic_w/3908.jpg" />
    </q-carousel>
  </div>
      <q-form @submit.prevent="Submit">
        <q-card-section>
          <!-- linha01 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadPet.nomePet" outlined label="Nome Pet" />
            </div>
            <div class="q-pa-xs col-6">
              <q-select
                label="Espécie"
                transition-show="scale"
                transition-hide="scale"
                outlined
                v-model='cadPet.especie'
                :options="especie"
              />
            </div>
          </div>
          <!-- linha02 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <div class="q-pa-xs col-6">
                <q-input v-model="cadPet.raca" outlined label="Raça" />
              </div>
            </div>
            <div class="q-pa-md col-6 text-center">
              <q-radio v-model="cadPet.sexo" val="macho" label="Macho" />
              <q-radio v-model="cadPet.sexo" val="femea" label="Fêmea" />
            </div>
          </div>
          <!-- linha03 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadPet.peso" outlined label="Peso" />
            </div>
            <div class="q-pa-xs col-6">
              <q-input v-model="cadPet.idade" outlined label="Idade" />
            </div>
          </div>
          <!-- butao -->
          <div class="row justify-end">

              <q-btn @click="petSave" class="q-mt-md" color="grey-10" label="Salvar" />

          </div>
        </q-card-section>
      </q-form>
    </q-card>
  </q-page>
</template>
<script>
export default {
  data () {
    return {
      cadPet: {
        nomePet: '',
        especie: '',
        sexo: '',
        raca: '',
        peso: '',
        idade: ''

      },
      slide: 1,
      especieModel: null,
      especie: ['Canino', 'Felino', 'Roedor', 'Ave', 'Peixe']
    }
  },
  methods: {
    petSave () {
      console.log(this.cadPet)
    }
  }
}
</script>

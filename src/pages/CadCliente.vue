<template>
  <q-page class="row flex justify-center bg-pink-1">
    <q-card class="q-pa-md my-card bg-grey-2 text-black shadow-1 col-10">
      <q-form @submit.prevent="Submit">
        <q-card-section>
          <!-- linha01 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.nomeCLiente" outlined label="Nome Cliente" />
            </div>
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.telefone" outlined label="Telefone pra contato" />
            </div>
          </div>
          <!-- linha02 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.email" outlined label="Email" />
            </div>
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.cep" outlined label="Cep" />
            </div>
          </div>
          <!-- linha03 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.logradouro" outlined label="Logradouro" />
            </div>
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.bairro" outlined label="Bairro" />
            </div>
          </div>
          <!-- linha04 -->
          <div class="row">
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.cidade" outlined label="Cidade" />
            </div>
            <div class="q-pa-xs col-6">
              <q-input v-model="cadCliente.estado" outlined label="Estado" />
            </div>
          </div>
                    <!-- butao -->
          <div class="row justify-end">

              <q-btn @click="clienteSave" class="q-mt-md" color="grey-10" label="Salvar" />

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
      cadCliente: {
        nomeCLiente: '',
        telefone: '',
        email: '',
        cep: '',
        logradouro: '',
        bairro: '',
        cidade: '',
        estado: ''
      }
    }
  },
  methods: {
    clienteSave () {
      console.log(this.cadCliente)
    }
  }
}
</script>

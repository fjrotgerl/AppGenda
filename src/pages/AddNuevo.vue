<template>
  <q-page class="flex">
    <div style="margin: 10px auto; width: 90%;">
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-md"
      >
        <p class="text-h6">Título</p>
        <q-input
          filled
          v-model="name"
          label="Título"
        />

        <p class="text-h6">Fecha</p>
        <div class="flex flex-center">
          <q-date v-model="date" style="width: 90%; margin-bottom: 20px;"/>
        </div>

        <p class="text-h6">Imágenes</p>
        <div class="flex flex-center">
          <q-uploader
            url="http://localhost:4444/upload"
            label="Subir imagenes"
            multiple
            style="width: 90%; margin-bottom: 20px;"
          />
        </div>

        <div class="flex flex-center">
          <q-btn label="Añadir" type="submit" color="primary" class="full-width"/>
        </div>

      </q-form>
    </div>

  </q-page>
</template>

<style>
</style>

<script>
  export default {
    data () {
      return {
        name: null,
        age: null,
        accept: false,
        date: ""
      }
    },
    methods: {
      onSubmit () {
        if (this.accept !== true) {
          this.$q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'fas fa-exclamation-triangle',
            message: 'You need to accept the license and terms first'
          })
        }
        else {
          this.$q.notify({
            color: 'green-4',
            textColor: 'white',
            icon: 'fas fa-check-circle',
            message: 'Submitted'
          })
        }
      },
      onReset () {
        this.name = null
        this.age = null
        this.accept = false
      }
    }
  }
</script>

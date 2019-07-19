<template>
  <q-page class="flex">
    <q-card style="width: 90%; height: 100%; margin: 10px auto;">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" @click="$router.push('/fotos')">
        <div class="absolute-bottom">
          <div class="text-h6">Casa 1</div>
          <div class="text-subtitle2">21/05/2019</div>
        </div>
      </q-img>

      <q-card-actions class="flex flex-center">
        <p class="flex flex-center">Texto de exemplo</p>
      </q-card-actions>
    </q-card>

  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex'
}
</script>

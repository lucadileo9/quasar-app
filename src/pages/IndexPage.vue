<template>
  <q-page class="flex flex-center">
    <div class="row">
      <q-input
        standout
        v-model="text"
        label="Counter"
        placeholder="Counter"
        input-class="text-center text-h5"
      />
    </div>

    <div class="row full-width">
      <div class="col text-center item-center">
        <q-btn round color="secondary" icon="remove" size="xl" class="my-hover-button" />
      </div>
      <div class="col text-center text-h2">100</div>
      <div class="col text-center">
        <q-btn round color="secondary" icon="add" size="xl" />
      </div>
    </div>

    <div class="row">
      <q-btn round icon="restart_alt" class="my-hover-button" color="secondary" size="xl" />
    </div>
  </q-page>
</template>

<script setup>
//
</script>

<style scoped>
/* Stile che si applica solo al passaggio del mouse */
.my-hover-button:hover {
  background-color: #040dfd !important; /* Esempio: cambia colore di sfondo (Arancione) */
  /* N.B.: senza !important, il colore di sfondo non cambierà */

  /* Potresti voler cambiare anche il colore dell'icona/testo */
  color: rgb(20, 20, 20) !important; /* Esempio: cambia colore dell'icona/testo a bianco */
}

.q-page {
  max-width: 700px;
  margin: 0 auto;
  padding: 20px;
}
</style>

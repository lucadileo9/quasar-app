<template>
  <q-page class="flex flex-center">
    <div class="row">
      <q-input
        standout
        label="Counter"
        placeholder="Counter"
        input-class="text-center text-h5"
        v-model:model-value="data.name"
      />
    </div>

    <div class="row full-width">
      <div class="col text-center item-center">
        <q-btn round color="secondary" icon="remove" size="xl" class="my-hover-button" @click="decrement"/>
      </div>
      <div class="col text-center text-h2">{{ data.counter }}</div>
      <div class="col text-center">
        <q-btn round color="secondary" icon="add" size="xl" @click="increment" />
      </div>
    </div>

    <div class="row">
      <q-btn round icon="restart_alt" class="my-hover-button" color="secondary" size="xl" @click="reset"/>
    </div>
  </q-page>
</template>

<script setup>
//
/* Imports */
  import { reactive } from 'vue';

  /* Data */
  const data = reactive({
    counter : 40,
    name: 'Counter',
  });

  /* Methods */
  const increment = () => {
    data.counter++;
  };
  const decrement = () => {
    data.counter--;
  };
  const reset = () => {
    data.counter = 0;
  };
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

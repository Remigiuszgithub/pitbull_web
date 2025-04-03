<script setup>
import { ref } from 'vue';

const props = defineProps({
    showLogo: {
        type: Boolean,
        default: true
    }
});

// Tworzymy lokalny stan, aby móc nim zarządzać w komponencie
const stateModal = ref(props.showLogo);

// Funkcja do zamykania modala
const closeModal = () => {
    stateModal.value = false;
};
</script>

<template>
  <div id="myModal" class="modal" :class="{ 'is-active': stateModal }">
    <div class="modal background"></div>
    <div class="modal-content">
      <div class="box">
        <h1 class="title">To jest modal</h1>
        <p>Treść modala</p>
        <button class="button is-success" id="closeModal" @click="closeModal">Zamknij</button>
      </div>
    </div>
    <button class="modal-close is-large" aria-label="close" id="closeModal2" @click="closeModal"></button>  
  </div>
</template>

<style scoped>

</style>

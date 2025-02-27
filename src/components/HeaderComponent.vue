<!-- JavaScript del componente -->
<script setup>
import logo from '../assets/Sergio-Logo.png'; // Importar la imagen
import MenuIcon from '../assets/bars-solid.svg'
import ChevronUp from '../assets/chevron-up.svg'

import MenuOption from './MenuOption.vue'; // Importar el componente hijo

import { ref, onMounted, onUnmounted, watchEffect } from "vue";

const isMobile = ref(window.innerWidth < 800); // Define si es móvil
const isDesktop = ref(window.innerWidth > 800); // Define si es móvil
const isDeployed = ref(false);
// Función que actualiza el estado cuando cambia el tamaño
const checkScreenSize = () => {
  isMobile.value = window.innerWidth < 800; // Cambia a true si es menor a 768px
  isDesktop.value = window.innerWidth > 800; // Cambia a true si es mayor a 768px
  isDeployed.value = window.innerWidth > 800;
};

// Agregar evento de cambio de tamaño
onMounted(() => {
  window.addEventListener("resize", checkScreenSize);
});

// Limpiar el evento cuando el componente se destruye
onUnmounted(() => {
  window.removeEventListener("resize", checkScreenSize);
});

const showMenu = () => {
  isDesktop.value = !isDesktop.value;
  isDeployed.value = !isDeployed.value;
};
/**emit envia eventos personalizados desde un componente secundario a su componente principal.**/
const emit = defineEmits(["Navigate"]);
const page = ref("");

const Option_Clicked = (pageName) =>{
  page.value=pageName;
  emit("Navigate", page.value);
}
</script>

<!-- HTML template del componente -->
<template>
    <div class="Header-Container">
      <span class="LogoMenu-Container">
          <img :src="logo" alt="Sergio Hdz Logo" class="Logo-Header" @click="Option_Clicked('1')">

        <img :src="MenuIcon" alt="Menu" class="LogoHeader" v-if="isMobile && !isDeployed" @click="showMenu">
        <img :src="ChevronUp" alt="Close" class="LogoHeader" v-if="isMobile && isDeployed" @click="showMenu">
      </span>
      <div class="Menu-Container" v-show="isDesktop">
        <MenuOption OptionText="About Me" @click="Option_Clicked('2')"/>
        <MenuOption OptionText="Projects" @click="Option_Clicked('3')"/>
        <MenuOption OptionText="Contact" @click="Option_Clicked('4')"/>
      </div>
    </div>
</template>
<!-- Estilos CSS del componente -->
<style scoped>

@media only screen and (min-width: 800px)
{
    .Header-Container
    {
        width: auto;
        height: auto;
        padding: 16px 32px 16px 32px;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;

        gap: 40px;
        

    }
    .Logo-Header
    {
      height: 32px;
    }
    .Menu-Container
    {
      width: auto;

      display: flex;
      flex-direction: row;
      justify-content: space-between;
      gap: 28px;
    }
}
@media only screen and (max-width: 800px)
{
    .Header-Container
    {
        width: auto;
        height: auto;
        padding: 4px 0px 4px 0px;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        gap: 20px;
    }
    .LogoMenu-Container
    {
      width: 100%;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: space-between;

    }
    .Menu-Container
    {
      width: 100%;

      display: flex;
      flex-direction: column;
      justify-content: space-between;
      gap: 20px;
    }
    .Logo-Header
    {
      height: 32px;
    }
}
</style>
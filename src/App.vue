<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import Home from './components/HomeComponent.vue';
import AboutMe from './components/AboutMe.vue';
import PortfolioComponent from './components/PortfolioComponent.vue';
import MediaComponent from './components/MediaComponent.vue';
import { ref } from 'vue';

const showHome = ref(true);
const showAboutMe = ref(false);
const showProjects = ref(false);
const showContact = ref(false);


const currentPage = ref("");
const show_Pages = (destiny) =>{
  if(destiny==='1')
  {
    showHome.value = true;
    showAboutMe.value = false;
    showProjects.value = false;
    showContact.value = false;
  }
  else if(destiny==='2')
  {
    showHome.value = false;
    showAboutMe.value = true;
    showProjects.value = false;
    showContact.value = false;
  }
  else if(destiny==='3')
  {
    showHome.value = false;
    showAboutMe.value = false;
    showProjects.value = true;
    showContact.value = false;    
  }
  else if(destiny==='4')
  {
    showHome.value = false;
    showAboutMe.value = false;
    showProjects.value = false;
    showContact.value = true;    
  }
};
</script>

<template>
  <div class="Layout">
    <HeaderComponent @Navigate="show_Pages"/>
    <Home v-if="showHome" :visible="showHome" @Navigate="show_Pages"/>
    <PortfolioComponent v-if="showProjects" :visible="showProjects"/>
    <AboutMe v-if="showAboutMe" :visible="showAboutMe"/>
    <MediaComponent v-if="showContact" :visible="showContact"/>
  <!--div para el teleport aquí quedará el modal-->
  <div id="modals"></div>
  <PrimaryButton OptionText="Ejemplo"/>
  </div>

</template>

<style scoped>
  @media only screen and (min-width: 800px)
  {
      .Layout
      {
        display: flex;
        flex-direction: column;
        gap: 4vh; /* Espacio entre componentes */
      }
  }
  @media only screen and (max-width: 800px)
  {
      .Layout
      {
        display: flex;
        flex-direction: column;
        gap: 2vh; /* Espacio entre componentes */
      }
  }
</style>

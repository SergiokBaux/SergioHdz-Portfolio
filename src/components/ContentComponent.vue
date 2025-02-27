<script setup>
import AboutMe from './AboutMe.vue'; // Importar el componente hijo
import HomeComponent from './HomeComponent.vue';
import PortfolioComponent from './PortfolioComponent.vue';

</script>
<template>
    <div class="ContentContainer">
        <PortfolioComponent/>  
    </div>
</template>
<style scoped>
@media only screen and (min-width: 800px)
{
    .ContentContainer
    {
        width: 100%;
        height: 75vh;
        padding: 40px;
        background-color: rgba(133, 198, 236, 0.03);
        box-sizing: border-box;
        border: 2px solid var(--sergio-blue_60);
    }
}
@media only screen and (max-width: 800px)
{
    .ContentContainer
    {
        width: 100%;
        min-height: 75vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
        background-color: rgba(255, 255, 255, 0.1);
        box-sizing: border-box;
        border-radius: 12px;
        border: 1px solid #E7E7E7;
    }    
}

</style>
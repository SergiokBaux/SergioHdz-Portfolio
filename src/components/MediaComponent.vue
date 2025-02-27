<script setup>
import SocialMedia from './SocialMedia.vue';
import QuestionTitle from './QuestionTitle.vue';
</script>

<template>
    <div class="ContentContainer">
        <QuestionTitle principalquestion="WHERE?"/>
        <p class="text">Hey, Sergio here! If you want to contact me here are some options.</p>
        <div class="MediaContainer">
            <SocialMedia link="https://www.behance.net/sergiokbaux" social_network="Behance"/>
            <SocialMedia link="https://www.linkedin.com/in/sergio-hern%C3%A1ndez-65480527a/" social_network="LinkedIn"/>
            <SocialMedia link="https://drive.google.com/file/d/1Zfqv0pnLomGmAQqDm_DyD6Wnwotnh8w8/view" social_network="Resumé"/>
        </div>

        <SocialMedia link="a" social_network="sergiol.hernandezd@gmail.com"/>
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

        background-color: rgba(3, 3, 3, 0.2);
        display: flex;
        flex-direction: column;
        align-items: center;
        box-sizing: border-box;
        border: 2px solid var(--sergio-blue_60);
    }
    .text
    {
        color: var(--sergio-white);
        font-size: 20px;
        text-align: center;
        font-weight: normal;
    }
    .MediaContainer
    {
        height: 20vh;
        gap: 120px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
@media only screen and (max-width: 800px)
{
    .ContentContainer
    {
        width: 100%;
        height: 100vh;
        
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
        box-sizing: border-box;
        background-color: rgba(3, 3, 3, 0.2);
        border: 2px solid var(--sergio-blue_60);
    }
    .text
    {
        color: var(--sergio-white);
        font-size: 20px;
        text-align: center;
        font-weight: normal;
    }
    .MediaContainer
    {
        height: auto;
        gap: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
    }
}
</style>
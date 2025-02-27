<script setup>
import QuestionTitle from './QuestionTitle.vue';
import PrimaryButton from './PrimaryButton.vue';
import { ref } from 'vue';

const emit = defineEmits(["Navigate"]);
const page = ref("");

const Meet_Me = () =>{
    emit("Navigate", '2')
};
</script>


<template>
    <div class="ContentContainer">
        <QuestionTitle principalquestion="UX ENGINEER"/>
        <PrimaryButton OptionText="Meet Me" @click="Meet_Me"/>
    </div>
</template>
<style scoped>
/**Pantalla PC**/
@media only screen and (min-width: 800px)
{
    .ContentContainer
    {
        width: 100%;
        height: 75vh;
        padding: 40px;
        box-sizing: border-box;
        gap: 40px;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .SubTitle
    {
        color: var(--sergio-white);
        font-weight: normal;
    }
}
/**Dispositivos Moviles pequeños**/
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
        box-sizing: border-box;
        gap: 60px;

    } 
    .SubTitle
    {
        color: var(--sergio-white);
        font-weight: normal;
    }

}

</style>
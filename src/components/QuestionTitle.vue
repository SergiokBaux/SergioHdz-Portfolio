<script setup>
const props = defineProps({
  principalquestion: {
    type: String,
    required: false
  }
});
</script>
<template>
    <div class="QuestionContainer">
        <div class="Sergio-Title">‎SERGIO HDZ</div>
        <div class="PhoneContainer">
        <ul class="PrincipalQuestionContainer animation">
            <li class=""><div class="Title">WHAT?</div></li>
            <li class=""><div class="Title">WHO?</div></li>
            <li class=""><div class="Title">WHERE?</div></li>
            <li class=""><div class="Title enphasis">‎{{principalquestion}}</div></li>
        </ul> 
        </div>
    
    </div>

</template>
<style scoped>
@media only screen and (min-width: 800px)
{
    .QuestionContainer
    {
        width: 100%;
        height: 10vh;
        display: flex;
        flex-direction: row;
        color: var(--sergio-white);
        justify-content: center;
        align-items: center;
        overflow: hidden;
        letter-spacing: 20px;
    }
    .PrincipalQuestionContainer
    {
        height: 6vh;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        margin: 0%;
        padding: 0%;
    }
    ul li
    {
        list-style: none;
    }
    .Sergio-Title
    {
        height: 6vh;
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: lighter;
        font-size: 36px;
        letter-spacing: 20px;
    }
    .Title
    {
        height: 10vh;
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        font-size: 36px;
    }
    .animation
    {
        animation: scroll-auto 2.6s ease-in-out 1;
        animation-fill-mode: forwards;
    }
    .enphasis
    {
        color: var(--sergio-pink_60);
    }
    @keyframes scroll-auto {
        0%{}
        25%{transform: translate(0px, 0vh);}
        50%{transform: translate(0px, -10vh);}
        75%{transform: translate(0px, -20vh);}
        100%{transform: translate(0px, -30vh);}
    }
}
    @media only screen and (max-width: 800px)
    {
    .QuestionContainer
    {
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: column;
        color: var(--sergio-white);
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }
    .PrincipalQuestionContainer
    {
        height: 10vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        margin: 0%;
        padding: 0%;

    }
    .PhoneContainer
    {
            overflow: hidden;
            height: 10vh;
    }
    ul li
    {
        list-style: none;
    }
    .Sergio-Title
    {
        height: 10vh;
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: lighter;
        font-size: 28px;
        letter-spacing: 16px;
        text-align: center;

    }
    .Title
    {
        height: 10vh;
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        font-size: 28px;
        letter-spacing: 20px;
        text-align: center;
    }
    .animation
    {
        animation: scroll-auto 3.5s ease-in-out 1;
        animation-fill-mode: forwards;
    }
    .enphasis
    {
        color: var(--sergio-pink_70);
    }
    @keyframes scroll-auto {
        0%{}
        25%{transform: translate(0px, 0vh);}
        50%{transform: translate(0px, -10vh);}
        75%{transform: translate(0px, -20vh);}
        100%{transform: translate(0px, -30vh);}
    }
    }
</style>
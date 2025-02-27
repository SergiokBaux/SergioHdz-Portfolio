<script setup>
import QuestionTitle from './QuestionTitle.vue';
</script>

<template>
        <div class="ContentContainer">
            <div class="ContainerComplete">
                <QuestionTitle principalquestion="WHO?" />
                <div class="Container">
                    <div class="TextContainer">
                    <p class="Subtitle">I'm passionate about crafting intuitive and engaging digital experiences.</p>
                    <p class="Text">
                        Hey there! I’m a Computer Engineer with a focus on UX design and front-end development. I specialize in interface design, user research, and web development, working with tools like Figma, HTML, CSS, and JavaScript.
                        <br><br>
                        I thrive on creating accessible and functional digital experiences, integrating user-centered design principles, continuous improvement, and collaborative work within interdisciplinary teams.
                    </p>
                    </div>
                    <div class="ImageContainer">
                        <img src="../assets/Me.png" alt="" class="Image">
                    </div>
                </div>
            </div>
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
            box-sizing: border-box;
            border: 2px solid var(--sergio-blue_60);
        }
        .ContainerComplete
        {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            align-content: center;
        }
        .Container
        {
            width: 100%;
            height: auto;
            box-sizing: border-box;
            inset: 0;
            display: flex;
            flex-direction: row;
            align-items: center;
        }
        .TextContainer
        {
            width: 70%;
            height: 100%;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: baseline;
            justify-content: center;
            box-sizing: border-box;
        }
        .Text
        {
            font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
            font-size: 20px;
            color: var(--sergio-white);

        }
        .Subtitle
        {
            font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
            font-size: 20px;
            font-weight: 550;
            color: var(--sergio-pink_40);

        }
        .ImageContainer
        {
            width: 30%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .Image
        {
            width: 35vh;
            height: 35vh;
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
            background-color: rgba(3, 3, 3, 0.2);
            box-sizing: border-box;
            border: 2px solid var(--sergio-blue_60);
        }  
        .Container
        {
            width: 100%;
            height: 100%;
            box-sizing: border-box;
            inset: 0;
            display: flex;
            flex-direction: column-reverse;
        }
        .TextContainer
        {
            width: 100%;
            height: auto;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            box-sizing: border-box;
        }
        .Subtitle
        {
            font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
            font-size: 20px;
            font-weight: 550;
            color: var(--sergio-pink_40);
        }
        .Text
        {
            font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
            font-size: 20px;
            color: var(--sergio-white);
        }
        .ImageContainer
        {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .Image
        {
            width: 160px;
            height: 160px;
        }
    }
</style>
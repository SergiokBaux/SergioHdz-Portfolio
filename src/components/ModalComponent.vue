<script setup>
import PrimaryButton from './PrimaryButton.vue';

const props = defineProps({
    visible: {
    type: Boolean,
    required: true
    },
    project_title: {
    type: String,
    required: true
    },
    project_picture: {
    type: String,
    required: true
    },
    project_description: {
    type: String,
    required: true
    },
    project_link:{
        type: String,
        required: true
    }
});
const emit = defineEmits(["close"]);

const close = () =>{
    emit("close");
};
</script>

<template>
    <teleport to='#modals' >
    <div class="Overlay_Background" v-if="visible">
        <div class="Modal">
                <!---Icono--->
                <div class="Close_Container">
                    <button @click="close" class="Close_Button">Close</button>
                </div>
                    <!---Titulo--->
                    <div class="Title_Container">
                        <h1>{{project_title}}</h1>
                    </div>

            <div class="Image_Container">
                <!---imagen--->
                <img v-bind:src="'/src/assets/ImgProjects/' + project_picture + '.jpg'" alt="" class="Project_Picture">
            </div>
            <div class="Paragraph_Container">
                <!---parrafo--->
                <p class="Description_Text">{{project_description}}</p>
            </div>
            <a :href="project_link" class="link">
                <PrimaryButton OptionText="View More >"/>
            </a>

        </div>
    </div>
    </teleport>
</template>
<style scoped>
@media only screen and (min-width: 800px)
{
    .link
    {
      width: 100%;
      height: auto;
      text-decoration: none;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .Close_Container
    {
        display: flex;
        flex-direction: row;
        align-items: baseline;
    }
    .Overlay_Background
    {
        position: fixed;
        top: 0%;
        left: 0%;
        width: 100vw;
        height: 100vh;

        background: rgba(0, 0, 0, 0.8); /* Color negro con opacidad */
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }
    .Modal
    {
        background-color: var(--sergio-black);
        border-left: 4px solid var(--sergio-white);

        
        right: 0;
        top: 0;
        position: fixed;
        width: 40vw;
        height: 94vh;

        padding: 20px 12px 20px 12px;
        display: flex;
        flex-direction: column;
        gap: 8px;
        overflow-y: scroll;
    }
    .Close_Button
    {
        color: var(--sergio-white);
        background-color: transparent;
        border: none;

        letter-spacing: 8px;
        text-transform: uppercase;
    }
    .Title_Container
    {
        width: 100%;
        height: auto;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        color: var(--sergio-blue_50);
    }
    .Image_Container
    {
        width: 100%;
        height: fit-content;
    }
    .Project_Picture
    {
        width: 100%;
        height: auto;
    }
    .Paragraph_Container
    {
        width: 100%;
        height: fit-content;
        padding: 0px 0px 40px 0px;
    }
    .Description_Text
    {
        color: var(--sergio-white);
        font-size: 16px;
        text-align: justify;
    }
}

@media only screen and (max-width: 800px)
{
    .link
    {
      width: 100%;
      height: auto;
      text-decoration: none;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .Overlay_Background
    {
        position: fixed;
        top: 0%;
        left: 0%;
        width: 100vw;
        height: 100vh;

        background: rgba(0, 0, 0, 0.8); /* Color negro con opacidad */
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .Modal
    {
        background-color: black;
        border-left: 4px solid white;

        right: 0;
        top: 0;
        position: fixed;
        width: 80vw;
        height: 100vh;
        padding: 20px 16px 20px 16px;

        display: flex;
        flex-direction: column;
        gap: 20px;
        overflow-y: scroll;
    }
    .Close_Button
    {
        color: var(--sergio-white);
        background-color: transparent;
        border: none;

        letter-spacing: 8px;
        text-transform: uppercase;
    }
    .Title_Container
    {
        width: 100%;
        height: auto;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        color: var(--sergio-blue_50);
    }
    .Image_Container
    {
        width: 100%;
        height: fit-content;
    }
    .Project_Picture
    {
        width: 100%;
        height: auto;
    }
    .Paragraph_Container
    {
        width: 100%;
        height: fit-content;
    }
    .Description_Text
    {
        color: var(--sergio-white);
        font-size: 16px;
        text-align: justify;
    }

}
</style>
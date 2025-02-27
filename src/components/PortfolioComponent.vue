<script setup>
import { ref } from 'vue';
import QuestionTitle from './QuestionTitle.vue';
import ProjectPreview from './ProjectPreview.vue';
import ModalComponent from './ModalComponent.vue';

/** Variables para mostrar el modal y la información del Proyecto**/
const mostrarModal = ref(false);
const projectInformation = ref({ title: "", picture: "", description: "", link:""});
/** Función para mostrar el modal y la información del Proyecto**/
const openModal = (project) => {
    projectInformation.value = project;
    mostrarModal.value = true;
};

</script>
<template>
    <div class="ContentContainer" id="ContentContainer">
        <div class="Portfolio">
            <QuestionTitle principalquestion="WHAT?"/>
                <div class="WrapperContainer">
                    <div class="Wrapper">
                        <!---Dticket--->
                        <ProjectPreview @receiveMessage="() => openModal({ 
                            title: 'DTicket', 
                            picture: 'DTicket_image', 
                            description: 'Have you ever wanted to buy tickets for a concert, only to find they are sold out? Dticket is a mobile UX design project that allows you to buy tickets for concerts you want to attend. It also enables you to acquire tickets on the resale market and sell your own tickets in a secure way. DTicket is a mobile app designed as a project to obtain Google’s User Experience Design certification.',
                            link:'https://www.behance.net/gallery/218333415/DTicket'
                        })" 
                        preview_src="DTicket" />
                        <!---LCA--->
                        <ProjectPreview @receiveMessage="() => openModal({ 
                            title: 'LCA', 
                            picture: 'LCA_image', 
                            description: 'Have you ever needed a computer urgently in your school? The LCA project (Applied Computing Laboratory) responds to this need with a UX/UI solution designed for the work centers of the civil area of the Faculty of Engineering of the UASLP. Its objective is to facilitate equipment loans, organize classrooms and keep an efficient control of technological resources and administrative activities.',
                            link:'https://www.behance.net/gallery/200256025/Laboratorio-de-Computacion-Aplicada-LCA'
                        })" 
                        preview_src="LCA" />
                        <!---FiestApp--->
                        <ProjectPreview @receiveMessage="() => openModal({ 
                            title: 'FiestApp', 
                            picture: 'FiestApp_image', 
                            description: 'FiestApp is an application to find parties near you, you can organize your own parties and share your invitation through the social network of your choice.',
                            link:'https://www.behance.net/gallery/200719105/FiestApp'

                        })" 
                        preview_src="FiestApp" />
                </div>
            </div>
        </div>
    </div>
    <ModalComponent v-if="mostrarModal" :visible="mostrarModal" :project_link="projectInformation.link" :project_title="projectInformation.title" :project_picture="projectInformation.picture" :project_description="projectInformation.description" @close="mostrarModal = false"/>
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
    .Portfolio
    {
        width: 100%;
        height: 100%;
    }
    .WrapperContainer
    {
        height: 52vh;
        overflow: hidden;
        overflow-x: hidden;
        overflow-y: scroll; /* Solo scroll vertical */
    }
    .Wrapper
    {
        height: auto;
        display: grid;
        box-sizing: border-box;
        grid-template-columns: repeat(3, 1fr);
        gap: 40px;
        padding: 20px 0px;
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
        box-sizing: border-box;
        background-color: rgba(3, 3, 3, 0.2);
        border: 2px solid var(--sergio-blue_60);
    } 
    .Portfolio
    {
        width: 100%;
        height: 100%;
    }
    .WrapperContainer
    {
        height: 52vh;
        overflow: hidden;
        overflow-x: hidden;
        overflow-y: scroll; /* Solo scroll vertical */
    }
    .Wrapper
    {
        height: 100%;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        padding: 20px 0px;
        gap: 40px;
    }
}
@media only screen and (max-width: 600px)
{
    .Portfolio
    {
        width: 100%;
        height: 100%;
    }
    .WrapperContainer
    {
        height: 52vh;
        overflow: hidden;
        overflow-x: hidden;
        overflow-y: scroll; /* Solo scroll vertical */
    }
    .Wrapper
    {
        height: auto;
        display: grid;
        box-sizing: border-box;
        grid-template-columns: repeat(1, 1fr);
        padding: 20px 0px;
        gap: 20px;
    }
}
</style>
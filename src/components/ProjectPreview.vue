<script setup>
    import ViewButton from './ViewButton.vue';

    const props = defineProps({
        preview_src: {
        type: String,
        required: true
        },
    });

    const emit = defineEmits(["ClickedButton"]);
    const notifyParent_ToShowModal = () => {
        emit("receiveMessage", 'true'); // Enviar un mensaje al padre
    };
</script>

<template>
        <div class="PreviewContainer">
            <img v-bind:src="'../src/assets/ImgProjects/' + preview_src + '.jpg'" alt="" class="imgProject">
            <ViewButton class="Hidden-Button" @click="notifyParent_ToShowModal"/>
        </div>
</template>
<style scoped>
@media only screen and (min-width: 800px)
{
    /** Contenedor principal**/
    .PreviewContainer
    {
        border-radius: 6px;
        position: relative;
    }
/** Clase de la imagen y hover**/
    .imgProject
    {
        height: auto;
        width: 100%;
        object-fit: cover;
        border: 1px solid var(--sergio-white);
        transition: all 0.6s ease; /* Duración de 0.5s y suavidad con 'ease' */
    }
    .PreviewContainer:hover .imgProject
    {
        filter: blur(1.25px); /* Aplica un desenfoque de 5 píxeles */
        opacity: 0.4; /* Reduce la opacidad al 70% */
        border: 1px solid var(--sergio-white);
        background-color: rgba(0, 0, 0, 0.5); /* Negro semitransparente al hacer hover */
    }
/** CSS del botón y **/
.Hidden-Button
    {
        position: absolute;
        top: 0%;
        transform: translateX(65%); /* Centra horizontalmente */
        
        display: flex;
        align-items: center;
        justify-content: center;

        opacity: 0; /* Oculto inicialmente */
        transition: all 0.6s ease; /* Suaviza el movimiento y la opacidad */
    }
    .PreviewContainer:hover .Hidden-Button
    {
        top: 40%; /* Posición final del botón al hacer hover */
        opacity: 1; /* Hazlo visible */
    }
}
@media only screen and (max-width: 800px)
{
    /** Contenedor principal**/
    .PreviewContainer
    {
        border-radius: 6px;
        position: relative;
    }
/** Clase de la imagen y hover**/
    .imgProject
    {
        height: auto;
        width: 100%;
        object-fit: cover;
        border: 1px solid var(--sergio-blue_70);
        transition: all 0.6s ease; /* Duración de 0.5s y suavidad con 'ease' */
    }
    .PreviewContainer:hover .imgProject
    {
        filter: blur(1.25px); /* Aplica un desenfoque de 5 píxeles */
        opacity: 0.4; /* Reduce la opacidad al 70% */
        background-color: rgba(0, 0, 0, 0.5); /* Negro semitransparente al hacer hover */
    }
/** CSS del botón y **/
.Hidden-Button
    {
        position: absolute;
        top: 0%;
        transform: translateX(50%); /* Centra horizontalmente */
        
        display: flex;
        align-items: center;
        justify-content: center;

        opacity: 0; /* Oculto inicialmente */
        transition: all 0.6s ease; /* Suaviza el movimiento y la opacidad */
    }
    .PreviewContainer:hover .Hidden-Button
    {
        top: 40%; /* Posición final del botón al hacer hover */
        opacity: 1; /* Hazlo visible */
    }
}

</style>

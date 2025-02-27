<!-- JavaScript del componente -->
<script setup>
const props = defineProps({
  OptionText: {
    type: String,
    required: true
  },
});


</script>

<!-- HTML template del componente -->
<template>
    <button class="PrimaryButton_Container">{{OptionText}}</button>
</template>
<!-- Estilos CSS del componente -->
<style scoped>
    .PrimaryButton_Container
    {
        border: 2px solid var(--sergio-pink_80);
        color: var(--sergio-pink_100);
        background-color: var(--sergio-pink_70);
        padding: 12px 24px 12px 24px;

        font-size: 14px;
        font-weight: bolder;
        text-transform: uppercase;
        text-align: center;
        letter-spacing: 11.52px;


        width: auto;
        height: fit-content;

        transition: 0.6s ease;
    }
    .PrimaryButton_Container:hover
    {
        border: 2px solid var(--sergio-pink_60);
        color: var(--sergio-pink_60);
        background-color: var(--sergio-pink_100);
        padding: 12px 24px 12px 24px;

        font-size: 14px;
        font-weight: bolder;
        text-transform: uppercase;
        text-align: center;
        letter-spacing: 11.52px;

        width: auto;
        height: auto;

    }

</style>
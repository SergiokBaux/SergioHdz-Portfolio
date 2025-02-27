<!-- JavaScript del componente -->
<script setup>
const props = defineProps({
  OptionText: {
    type: String,
    required: true
  },
  Link: {
    type: String,
    required: false,
  }
});


</script>

<!-- HTML template del componente -->
<template>
    <button class="Option_Principal_Container">{{OptionText}}</button>
</template>
<!-- Estilos CSS del componente -->
<style scoped>
    .Option_Principal_Container
    {
        border: 1px solid var(--sergio-white);
        color: var(--sergio-white);
        background-color: var(--sergio-pink_110);
        padding: 12px 24px 12px 24px;

        font-size: 14px;
        text-transform: uppercase;
        text-align: center;
        letter-spacing: 11.52px;


        width: auto;
        height: fit-content;

        transition: 0.6s ease;
    }
    .link
    {
      color: var(--sergio-white);
      text-decoration: none;
    }
    .Option_Principal_Container:hover
    {
        border: 1px solid var(--sergio-pink_50);
        color: var(--sergio-pink_50);
        background-color: var(--sergio-pink_110);
        padding: 12px 24px 12px 24px;

        font-size: 14px;
        font-weight:normal;
        text-transform: uppercase;
        letter-spacing: 11.52px;
        text-align: center;

        width: auto;
        height: auto;

    }

</style>
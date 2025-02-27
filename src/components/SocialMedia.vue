<script setup>
const props = defineProps({
    social_network: {
    type: String,
    required: true
    },
    link: {
        type: String,
        required: true
    }
});
</script>

<template>
    <a :href="link" class="Container">
        <img v-bind:src="'/src/assets/' + social_network + '.svg'" alt="" class="Social_Media_img">
        <div class="Label">{{social_network}}</div>
    </a>
</template>

<style scoped>
    .Container
    {
        width: auto;
        height: auto;

        display: flex;
        flex-direction: column;
        align-items: center;
        border: 1px solid transparent;
        gap: 12px;
        padding: 4px 20px 4px 20px;
        text-decoration: none;
        transition: 0.4s ease;
    }
    .Label
    {
        width: auto;
        height: auto;

        display: flex;
        flex-direction: row;
        align-items: center;

        font-size: 20px;
        font-weight: normal;
        color: var(--sergio-white);
    }
    .Social_Media_img
    {
        width: 36px;
        height: 36px;
    }
    .Container:hover
    {
        background-color:  var(--sergio-pink_100);
        border: 1px solid var(--sergio-pink_50);
    }
</style>

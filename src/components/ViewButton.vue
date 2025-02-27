<script setup>

</script>

<template>

        <button class="Button" onclick="">
            <div class="Icon-Container">
                <svg class="Icon" width="576" height="576" viewBox="0 0 576 576" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_1167_1644)">
                    <path d="M288 112C222.8 112 169.2 141.6 128.1 179.7C89.5999 215.5 62.9999 258 49.3999 288C62.9999 318 89.5999 360.5 128 396.3C169.2 434.4 222.8 464 288 464C353.2 464 406.8 434.4 447.9 396.3C486.4 360.5 513 318 526.6 288C513 258 486.4 215.5 448 179.7C406.8 141.6 353.2 112 288 112ZM95.3999 144.6C142.5 100.8 207.2 64 288 64C368.8 64 433.5 100.8 480.6 144.6C527.4 188.1 558.7 240 573.6 275.7C576.9 283.6 576.9 292.4 573.6 300.3C558.7 336 527.4 388 480.6 431.4C433.5 475.2 368.8 512 288 512C207.2 512 142.5 475.2 95.3999 431.4C48.5999 388 17.2999 336 2.4999 300.3C-0.800098 292.4 -0.800098 283.6 2.4999 275.7C17.2999 240 48.5999 188 95.3999 144.6ZM288 368C332.2 368 368 332.2 368 288C368 243.8 332.2 208 288 208C287.3 208 286.7 208 286 208C287.3 213.1 288 218.5 288 224C288 259.3 259.3 288 224 288C218.5 288 213.1 287.3 208 286C208 286.7 208 287.3 208 288C208 332.2 243.8 368 288 368ZM288 160C321.948 160 354.505 173.486 378.51 197.49C402.514 221.495 416 254.052 416 288C416 321.948 402.514 354.505 378.51 378.51C354.505 402.514 321.948 416 288 416C254.052 416 221.495 402.514 197.49 378.51C173.486 354.505 160 321.948 160 288C160 254.052 173.486 221.495 197.49 197.49C221.495 173.486 254.052 160 288 160Z" fill="currentColor"/>
                </g>
                <defs>
                <clipPath id="clip0_1167_1644">
                    <rect width="576" height="576" fill="currentColor"/>
                </clipPath>
                </defs>
            </svg>
            </div>

            <div class="Button-Text">Overview</div>
        </button> 


</template>

<style scoped>
    .Button
    {
        position: relative;
        height: 56px;
        width: auto;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;

        border: 2px solid var(--sergio-pink_80);
        background-color: var(--sergio-pink_70);

        padding: 12px;
        gap: 16px;

        transition: all 0.6s ease; /* Duración de 0.5s y suavidad con 'ease' */
    }

    .Button:hover
    {
        height: 56px;
        width: auto;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;

        border: 2px solid var(--sergio-pink_60);
        color: var(--sergio-pink_60);
        background-color: var(--sergio-pink_100);
        padding: 12px;
        gap: 16px;

        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        font-size: 18px;
    }
    .Icon
    {
        width: 28px;
        height: 28px;
        color: var(--sergio-pink_100);
        transition: color 0.6s ease;
    }
    .Icon-Container
    {
        width: 28px;
        height: 28px;
        color: var(--sergio-white); /* Color inicial del ícono */
        transition: color 0.6s ease;
    }
    .Button:hover .Icon-Container
    {
        color: var(--sergio-pink_60);
    }

    .Button-Text
    {
        width: auto;

        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        font-size: 18px;
        
        color: var(--sergio-pink_100);
        transition: all 0.6s ease; /* Duración de 0.5s y suavidad con 'ease' */

    }
    .Button:hover .Button-Text
    {
        font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        font-size: 18px;
        color: var(--sergio-pink_60);
    }
    .Button:hover .Icon
    {
        color: var(--sergio-pink_60);
    }


</style>
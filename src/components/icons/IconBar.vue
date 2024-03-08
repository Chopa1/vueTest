<template>
    <svg viewBox="0 0 922 10" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect class="rect1" x="0.5" rx="5" fill="#A2ACBE" fill-opacity="0.2"/>
        <rect class="rect2" x="0.5" width="638.262" rx="5" fill="#3C388D"/>
    </svg>
</template>

<style scoped>
    svg {
        width: 48.02083vw; /* Сделаем SVG растягиваемым по ширине контейнера */
        height: 11px;
    }

    rect {
        height: 10px;
    }

    .rect1 {
        width: 100%;
    }

    .rect2 {
        width: 69.2%;
    }

    @media (max-width: 1200px) {
        rect {
            height: 30px !important;
        }
    }
</style>
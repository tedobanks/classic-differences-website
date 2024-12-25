<script setup>
const props = defineProps({
    service: {
        type: Object,
        required: true,
        validator(value) {
            return value != null;
        },
        default: () => ({
            imageUrl: "",
            name: "",
            description: "",
        }),
    },
});
</script>

<template>
    <div class="service-container">
        <div
            class="image-container"
            :style="{ backgroundImage: `url(${service.imageUrl})` }"
        ></div>
        <div class="text-container">
            <h4 class="name">{{ service.name }}</h4>
            <div class="description-container">
                <p class="description">{{ service.description }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.service-container {
    width: 100%;
    height: 25rem;
    padding-inline: 4%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.service-container:nth-child(even) {
    flex-direction: row-reverse;
}

.service-container:nth-child(even) .text-container {
    padding-left: 0;
    padding-right: 1.25rem;
}

.image-container {
    height: 77%;
    width: 50%;
    background-color: white;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    border-radius: 1rem;
}
.text-container {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    padding-left: 1.25rem;
    gap: 0.625rem;
}

.name {
    color: var(--vt-c-red);
    font-size: 1.75rem;
    font-weight: 600;
    letter-spacing: 1.5px;
    line-height: 1;
}

.description-container {
    width: 100%;
}

.description {
    font-weight: 300;
    font-size: 1.125rem;
}

@media only screen and (max-width: 768px) {
    .service-container {
        flex-direction: column;
        height: fit-content;
        padding: 1.25rem;
        position: relative;
    }

    .service-container::before {
        content: "";
        position: absolute;
        height: 100%;
        width: 100%;
        background-color: var(--vt-c-red);
        opacity: 0.4;
        z-index: -3;
        border-radius: calc(22rem / 16);
        filter: blur(600px);
    }

    .service-container::after {
        content: "";
        position: absolute;
        height: calc(100% - 8px);
        width: calc(100% - 8px);
        background-color: var(--color-background);
        z-index: -1;
        border-radius: calc(22rem / 16);
    }
    
    .service-container:nth-child(even) {
        flex-direction: column;
    }
    
    .service-container:nth-child(even) .text-container {
        padding-left: 0;
        padding-right: 0;
    }

    .image-container {
        height: auto;
        width: 100%;
        aspect-ratio: 585 / 350;
        border-radius: 1rem;
        margin-bottom: 1.25rem;
    }

    .text-container {
        width: 100%;
        padding-left: 0;
        gap: 0.625rem;
    }
    
}
</style>

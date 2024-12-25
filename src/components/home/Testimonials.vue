<script setup>
import testimonials from "@/data/testimonials.json";
import { computed, ref } from "vue";

const activeIndex = ref(0);
const testimonialsList = ref(testimonials);

const currentTestimonial = computed(() => {
    return testimonialsList.value.find(
        (testimonial) => testimonial.id === activeIndex.value
    );
});

const prev = () => {
    if (activeIndex.value != 0) {
        activeIndex.value--;
    }
};

const next = () => {
    if (activeIndex.value < testimonialsList.value.length - 1) {
        activeIndex.value++;
    }
};
</script>

<template>
    <div class="container">
        <h2 class="section-title">testimonial</h2>
        <h3 class="tagline">Your Event, <br />Our Passion</h3>
        <div class="description-container">
            <p class="description">
                We prioritize each of our clients, ensuring their vision
                <br />comes to life with impeccable detail and care.
            </p>
        </div>
        <div class="carousel">
            <button class="direction-button prev" @click="prev">
                <img src="/images/caret.svg" alt="" />
            </button>
            <div class="carousel-container">
                <div class="text-container">
                    <h4 class="title">
                        {{ currentTestimonial.testimonial.title }}
                    </h4>
                    <p class="body">
                        {{ currentTestimonial.testimonial.body }}
                    </p>
                    <p class="name">{{ currentTestimonial.client.name }}</p>
                    <p class="type">
                        <span
                            v-if="currentTestimonial.client.subType != ''"
                            class="sub-type"
                            >{{ currentTestimonial.client.subType }},
                        </span>
                        <span class="main-type">{{
                            currentTestimonial.client.type
                        }}</span>
                    </p>
                </div>
                <div class="image-container">
                    <div
                        class="client-image"
                        :style="{
                            backgroundImage: `url(${currentTestimonial.image})`,
                        }"
                    ></div>
                </div>
            </div>
            <button class="direction-button next" @click="next">
                <img src="/images/caret.svg" alt="" />
            </button>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    position: relative;
    z-index: 1;
}
.container::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 31.25rem;
    aspect-ratio: 858/688;
    background-color: var(--vt-c-red);
    opacity: 0.5;
    border-radius: 50%;
    filter: blur(240px);
    z-index: -1;
}

.section-title {
    margin-top: 1.25rem;
}

.tagline {
    font-size: 3rem;
    font-weight: 700;
    letter-spacing: -1.5px;
    line-height: 1.1;
    text-align: center;
    margin-top: 1.25rem;
}

.description-container {
    width: 40%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 0.625rem;
}

.description {
    text-align: center;
    line-height: 1.3;
}

.carousel {
    width: 100%;
    height: 25rem;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin-top: 2.5rem;
    margin-bottom: 3.125rem;
}

.carousel-container {
    width: 70%;
    height: 100%;
    background-color: var(--color-background-secondary);
    border-radius: 2.5rem;
    color: var(--color-text-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    padding-inline: 1.25rem;
}

.text-container {
    width: 60%;
    display: flex;
    flex-direction: column;
    align-items: start;
}

.title {
    color: var(--vt-c-navy-blue);
    font-weight: 700;
    font-size: calc(24rem / 16);
    line-height: 1.1;
}

.body {
    margin-top: 0.625rem;
    margin-bottom: 2.5rem;
    color: var(--color-text-secondary);
    font-size: calc(16rem / 16);
    font-weight: 400;
    text-align: start;
    line-height: 1.2;
}

.name {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--color-text-secondary);
}

.type {
    opacity: 0.8;
    font-size: 1rem;
    color: var(--color-text-secondary);
}

.sub-type {
    font-weight: 400;
}

.main-type {
    font-weight: 700;
    text-transform: uppercase;
}

.image-container {
    width: 40%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.client-image {
    width: 80%;
    aspect-ratio: 1;
    border-radius: 50%;
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
}

.direction-button {
    width: 4rem;
    aspect-ratio: 1;
    background-color: var(--color-background-secondary);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
}

.direction-button img {
    width: 15px;
    aspect-ratio: 14.03/24.62;
    object-fit: contain;
    object-position: center;
}

.next img {
    transform: rotate(180deg);
}
</style>

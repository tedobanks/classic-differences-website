<script setup>
import testimonials from "@/data/testimonials.json"
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
            <button class="direction-button prev">
                <img src="/images/caret.svg" alt="" />
            </button>
            <div class="carousel-container"></div>
            <button class="direction-button next">
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
}

.carousel-container {
    width: 70%;
    height: 100%;
    background-color: var(--color-background-secondary);
    border-radius: 2.5rem;
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

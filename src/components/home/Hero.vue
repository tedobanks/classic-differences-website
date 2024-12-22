<template>
    <div class="container" id="home">
        <div class="tagline-container">
            <h1 class="tagline">Crafting Experiences</h1>
            <h1 class="tagline">that Last a Lifetime</h1>
        </div>
        <div class="description-container">
            <div class="description">
                We bring your vision to life with personalized event planning
                and seamless care services, ensuring every detail is handled
                with excellence.
            </div>
        </div>
        <button class="book-a-meeting">Book A Meeting</button>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: transparent;
    position: relative;
}

.container::before {
    content: "";
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    width: 31.25rem;
    aspect-ratio: 416/309;
    background-color: var(--vt-c-red);
    border-radius: 50%;
    opacity: 0.4;
    filter: blur(148px);
}

.tagline-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 3.125rem;
}

.tagline {
    text-align: center;
    font-weight: 700;
    font-size: 5.5rem;
    line-height: 1;
    letter-spacing: -3px;
    position: relative;
}

.tagline:first-child::after {
    content: "";
    width: 6rem;
    aspect-ratio: 1;
    position: absolute;
    right: -1.5rem;
    top: -110%;
    background-image: url("/images/star.svg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.tagline:last-child::before {
    content: "";
    width: 1rem;
    aspect-ratio: 1;
    position: absolute;
    left: 5%;
    bottom: -40%;
    background-image: url("/images/star.svg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.description-container {
    width: 36.25%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.description {
    text-align: center;
    font-size: 1.125rem;
    font-weight: 400;
    line-height: 1.3;
    margin-top: 3.125rem;
    position: relative;
}

.description::after {
    content: "";
    position: absolute;
    width: 1rem;
    aspect-ratio: 1;
    right: 7%;
    top: -20%;
    background-image: url("/images/star.svg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.book-a-meeting {
    width: 15.625rem;
    aspect-ratio: 298/64;
    background-color: var(--vt-c-red);
    color: var(--color-text-secondary);
    border-radius: 0.5rem;
    font-size: 1.125rem;
    font-weight: 500;
    cursor: pointer;
    border: none;
    margin-top: 3.125rem;
}
</style>

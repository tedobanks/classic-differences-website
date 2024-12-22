<template>
    <div class="container">
        <div class="items-wrapper">
            <div class="section-title">Why choose us?</div>
            <div class="tagline-description-container">
                <div class="tagline-container">
                    <div class="tagline">
                        Personalized Event & Care Solutions Tailored to Your
                        Needs
                    </div>
                </div>
                <div class="description-container">
                    <div class="description">
                        At Pato's Classic Differences, we bring your vision to
                        life with impeccable attention to detail. From event
                        planning to care home staffing, our services are crafted
                        to deliver exceptional results. Submit your requests,
                        and let us take care of everything, ensuring a seamless
                        and stress-free experience.
                    </div>
                    <button class="reach-out">Reach Out To Us</button>
                </div>    
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.items-wrapper {
    width: 90%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
}

.section-title {
    color: var(--vt-c-red);
    margin-top: 1.25rem;
    margin-bottom: 0.625rem;
}

.tagline-description-container {
    width: 100%;
    display: flex;
    align-items: start;
    justify-content: space-between;
}

.tagline-container {
    width: 60%;
}

.description-container {
    width: 40%;
    display: flex;
    flex-direction: column;
    justify-content: start;
    gap: 1.25rem;
}

.tagline {
    font-weight: 600;
    font-size: 3.125rem;
    line-height: 1;
}

.description {
    font-weight: 300;
    font-size: 1.125rem;
}

.reach-out {
    width: 12.5rem;
    aspect-ratio: 200/56;
    background-color: var(--vt-c-red);
    border-radius: 0.5rem;
    color: var(--color-text-secondary);
    cursor: pointer;
    border: none;
    font-size: 1.125rem;
}
</style>

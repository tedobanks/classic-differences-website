<template>
    <div class="container">
        <div class="main-footer"></div>
        <div class="footer-cta">
            <div class="title-container">
                <h3 class="title">Experience the Difference</h3>
            </div>
            <div class="description-container">
                <div class="description">
                    Discover how our expert team can bring your vision to life
                    with creative event planning, seamless execution, and
                    outstanding results.
                </div>
            </div>
            <div class="cta-button-container">
                <div class="cta-button"></div>
                <div class="cta-button"></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    position: relative;
}

.main-footer {
    width: 78%;
    height: 58vh;
    background-color: green;
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
}

.footer-cta {
    position: absolute;
    width: 80%;
    height: 63.6%;
    background-color: var(--vt-c-red-dark);
    border-radius: calc(35rem / 16);
    top: -31.8%; /* Adjust top to -31.8% of its height */
    left: 50%;
    transform: translate(-50%, 0); /* Remove vertical translation */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.title-container {
    width: 41%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.title {
    font-weight: 700;
    font-size: 4rem;
    letter-spacing: -3.5px;
    line-height: 1.1;
    text-align: center;
}

.description-container {
    margin-top: 0.625rem;
    width: 32.083%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.description {
    font-weight: 400;
    line-height: 1.3;
    text-align: center;
}

.cta-button-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1.875rem;
    margin-top: 1.875rem;
}

.cta-button {
    background-color: var(--vt-c-red);
    width: 11.59375rem;
    height: 3.5rem;
    border-radius: 0.5rem;
    color: var(--color-text-secondary);
}
</style>

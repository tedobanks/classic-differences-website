<script setup>
const perksList = [
    {
        image: "/images/rocket.svg",
        title: "Plan & Get Started",
        description:
            "Begin your journey with us, whether it's for a memorable event or a reliable care solution. Simply share your vision, and we'll manage every aspect, so you can focus on enjoying the experience.",
    },
    {
        image: "/images/pen.svg",
        title: "Expert Execution – on Time",
        description:
            "Our seasoned professionals are dedicated to delivering your projects with precision and on schedule. From flawless event setups to well-coordinated care services, every detail is handled with the highest level of care.",
    },
    {
        image: "/images/reload.svg",
        title: "Simple & Unlimited Revisions",
        description:
            "Your satisfaction is our top priority. We provide as many revisions as necessary to ensure that everything aligns perfectly with your expectations, whether for event design or service arrangements.",
    },
];
</script>

<template>
    <div class="container" id="perks">
        <div class="items-wrapper">
            <h2 class="section-title">Why choose us?</h2>
            <div class="tagline-description-container">
                <div class="tagline-container">
                    <h3 class="tagline">
                        Personalized Event & Care Solutions Tailored to Your
                        Needs
                    </h3>
                </div>
                <div class="description-container">
                    <div class="description">
                        At Classic Differences, we bring your vision to
                        life with impeccable attention to detail. From event
                        planning to care home staffing, our services are crafted
                        to deliver exceptional results. Submit your requests,
                        and let us take care of everything, ensuring a seamless
                        and stress-free experience.
                    </div>
                    <a
                        href="mailto:classicdifferenceslimited@gmail.com?subject=General Inquiry&body=Hello Classic Differences,%0D%0A%0D%0AI'm interested in learning more about your services.%0D%0A%0D%0AService Interest:%0D%0AMessage:"
                        class="reach-out-wrapper"
                    >
                        <button class="reach-out">Reach Out To Us</button>
                    </a>
                </div>
            </div>
        </div>
        <div class="perks-container">
            <div v-for="(perk, index) in perksList" :key="index" class="perk">
                <div class="image-container">
                    <img :src="perk.image" alt="" />
                </div>
                <h4 class="perk-title">{{ perk.title }}</h4>
                <p class="perk-description">{{ perk.description }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.items-wrapper {
    width: 90%;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    margin-bottom: 3rem;
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

.reach-out-wrapper {
    text-decoration: none;
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

.perks-container {
    width: 90%;
    display: flex;
    align-items: start;
    justify-content: space-between;
    margin-bottom: 2.5rem;
}

.perk {
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    position: relative;
}

.image-container {
    width: calc(80rem / 16);
    aspect-ratio: 1;
    border-radius: 50%;
    background-color: var(--vt-c-red);
    margin-bottom: 1.25rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

.perk:first-child::after,
.perk:nth-child(2)::after {
    content: "";
    width: 100%;
    aspect-ratio: 324 / 8;
    position: absolute;
    left: 2.5rem;
    top: 2.5rem;
    background-image: url("/images/arrow.svg");
    background-size: cover;
    background-color: transparent;
    background-repeat: no-repeat;
    background-position: center;
    z-index: -1;
}

.image-container img {
    width: 45%;
    aspect-ratio: 1;
}

.perk-title {
    font-weight: 500;
    font-size: calc(24rem / 16);
    margin-bottom: 0.625rem;
}

.perk-description {
    width: 80%;
}

@media only screen and (max-width: 768px) {
    .container {
        width: 100%;
        padding-inline: 1.25rem;
    }

    .section-title {
        margin-top: 5rem;
    }

    .tagline-description-container {
        flex-direction: column;
    }

    .tagline-container,
    .description-container {
        width: 100%;
    }

    .tagline {
        margin-bottom: 1.25rem;
    }

    .perks-container {
        flex-direction: column;
        gap: 2.5rem;
    }

    .perk {
        width: 100%;
        height: fit-content !important;

        margin-bottom: 5rem;
    }

    .perk:first-child::after,
    .perk:nth-child(2)::after {
        top: auto;
        left: -8%;
        bottom: -3.75rem;
        transform: rotate(90deg);
        width: 6.25rem;
        background-size: cover;
    }
}
</style>

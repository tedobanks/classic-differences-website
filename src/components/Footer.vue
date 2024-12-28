<script setup>
import { computed } from "vue";

const currentYear = computed(() => new Date().getFullYear());
const navLinks = [
    { path: "#home", name: "Home" },
    { path: "#services", name: "Services" },
    { path: "#perks", name: "Why choose us?" },
    { path: "#testimonials", name: "Testimonials" },
    { path: "#faq", name: "FAQs" },
    { path: "", name: "Privacy Policy" },
];
</script>

<template>
    <div class="container">
        <!-- Main Footer -->
        <div class="main-footer">
            <div class="basic-footer-info">
                <div class="company-info">
                    <div class="company-info-logo"></div>
                    <p class="company-info-about">
                        Classic Differences - A premier events and care services
                        provider operating across the UK and Nigeria, delivering
                        exceptional experiences and compassionate care solutions
                        since 2020. Our dual expertise sets us apart in creating
                        memorable moments and nurturing environments.
                    </p>
                </div>
                <div class="company-contact">
                    <div class="contact-item">
                        <img src="/images/mail.svg" alt="" />
                        <a
                            href="mailto:classicdifferenceslimited@gmail.com?subject=Inquiry&body=Hi there, I'm contacting you through your website..."
                            target="_blank"
                            >classicdifferenceslimited@gmail.com</a
                        >
                    </div>
                    <div class="contact-item">
                        <img src="/images/phone.svg" alt="" />
                        <p>07476218341</p>
                    </div>
                </div>
            </div>

            <hr class="main-footer-divider" />

            <div class="sitemap">
                <div class="nav-links">
                    <a
                        v-for="(item, index) in navLinks"
                        :key="index"
                        :href="item.path"
                        >{{ item.name }}</a
                    >
                </div>
                <div class="copy-right-info">
                    <p>
                        &copy; {{ currentYear }} Classic Differences - All Right
                        Reserved
                    </p>
                </div>
            </div>
        </div>

        <!-- Footer CTA -->
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
                <a
                    href="https://wa.me/447476218341?text=I%20want%20to%20enquire%20about%20..."
                    class="cta-button-wrapper"
                    target="_blank"
                ></a>
                <div class="cta-button">
                    <img src="/images/whatsapp.png" alt="" class="whatsapp" />
                    <p>WhatsApp</p>
                </div>

                <!-- Second Button -->
                <a
                    href="mailto:classicdifferenceslimited@gmail.com?subject=Inquiry&body=Hi there, I'm contacting you through your website..."
                    class="cta-button-wrapper"
                    target="_blank"
                >
                    <div class="cta-button">
                        <img src="/images/mail.svg" alt="" />
                        <p>Email</p>
                    </div>
                </a>
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
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
}

.basic-footer-info {
    width: 100%;
    display: flex;
    align-items: start;
    justify-content: space-between;
}

.company-info {
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    gap: 0.625rem;
}

.company-info-logo {
    width: 70%;
    aspect-ratio: 895/274;
    background-image: url("/images/logo-light-mode.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: start;
}

.company-info-about {
    font-size: 0.875rem;
}

.main-footer-divider {
    width: 100%;
    height: 0.5px;
    color: var(--color-text);
    margin-top: 2.5rem;
}

.company-contact {
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    gap: 1.25rem;
}

.contact-item {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: start;
}

.contact-item img {
    width: 1.25rem;
    aspect-ratio: 1;
    object-fit: cover;
    object-position: center;
    margin-right: 0.625rem;
    filter: invert(1);
}

.contact-item a {
    text-decoration: none;
    color: var(--color-text);
}

.sitemap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-grow: 1;
}

.nav-links {
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 0.9375rem;
}

.nav-links a {
    text-decoration: none;
    color: var(--color-text);
    font-size: 0.875rem;
}

.copy-right-info {
    display: flex;
    align-items: center;
    justify-content: start;
}

.copy-right-info p {
    font-size: 0.875rem;
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

.cta-button-wrapper {
    text-decoration: none;
}

.cta-button {
    background-color: var(--vt-c-red);
    width: 11.59375rem;
    height: 3.5rem;
    border-radius: 0.5rem;
    color: var(--color-text-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.3125rem;
    cursor: pointer;
}

.cta-button img {
    width: 1.25rem;
    aspect-ratio: 1;
}

.cta-button p {
    color: var(--vt-c-white);
}

@media only screen and (prefers-color-scheme: dark) {
    .company-info-logo {
        background-image: url("/images/logo-dark-mode.png");
    }

    .company-contact img {
        filter: none;
    }

    .whatsapp {
        filter: invert(1);
    }
}

@media only screen and (max-width: 768px) {
    .container {
        display: flex;
        flex-direction: column-reverse;
        gap: 2.5rem;
        padding-block: 2.5rem;
    }

    .main-footer,
    .footer-cta {
        position: relative;
        top: auto;
    }

    .basic-footer-info,
    .sitemap,
    .nav-links,
    .cta-button-container {
        flex-direction: column;
    }

    .basic-footer-info,
    .company-info {
        gap: 1.25rem;
    }

    .company-info,
    .company-contact,
    .title-container,
    .description-container {
        width: 100%;
    }

    .company-contact {
        gap: 0.625rem;
    }

    .main-footer,
    .footer-cta {
        width: calc(100% - 2.5rem);
    }

    .main-footer-divider {
        margin-block: 2.5rem;
    }

    .sitemap {
        align-items: start;
        gap: 1.25rem;
    }

    .nav-links {
        align-items: start;
        gap: 0.625rem;
    }

    .footer-cta {
        padding: 1.25rem;
        height: auto;
    }

    .title {
        font-size: 2.5rem;
    }

    .cta-button-container {
        width: 100%;
        gap: 1.25rem;
    }

    .cta-button {
        width: 100%;
        border-radius: calc(26.25rem / 16);
    }
}
</style>

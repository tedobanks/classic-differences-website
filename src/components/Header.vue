<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from "vue";

const windowWidth = ref(window.innerWidth);
const isMobile = computed(
    () => windowWidth.value >= 0 && windowWidth.value <= 768
);

const mobileMenuState = ref(false);

// Show menu if it's desktop OR if it's mobile and menu is toggled
const shouldShowMenu = computed(() => !isMobile.value || mobileMenuState.value);

const paths = [
    {
        name: "Contact",
        path: "/contact",
    },
];

const toggleMobileMenu = () => {
    mobileMenuState.value = !mobileMenuState.value;
};

onMounted(() => {
    window.addEventListener("resize", handleResize);
    console.log("mobileMenuState", mobileMenuState.value);
    console.log("isMobile: ", isMobile.value);
    console.log("shouldShowMenu: ", shouldShowMenu.value);
});

onBeforeUnmount(() => {
    window.removeEventListener("resize", handleResize);
});

function handleResize() {
    windowWidth.value = window.innerWidth;
}
</script>

<template>
    <div class="header-container">
        <div class="main-header-wrapper">
            <RouterLink to="/" class="logo-wrapper">
                <div class="logo"></div>
            </RouterLink>
            <div v-if="shouldShowMenu" class="nav-links">
                <div
                    v-if="isMobile"
                    class="close-icon"
                    @click="toggleMobileMenu"
                ></div>
                <RouterLink
                    v-for="(path, index) in paths"
                    :key="index"
                    :to="path.path"
                    class="nav-link"
                    >{{ path.name }}</RouterLink
                >
                <a
                    href="mailto:classicdifferenceslimited@gmail.com?subject=Request%20a%20Quote&body=Hi%20there,%0A%0AI%27m%20contacting%20you%20to%20request%20a%20quote%20through%20your%20website..."
                    class="cta-button"
                    >Request a Quote</a
                >
            </div>
            <div
                v-if="isMobile"
                class="menu-icon"
                @click="toggleMobileMenu"
            ></div>
        </div>
    </div>
</template>

<style scoped>
.header-container {
    width: 100%;
    height: fit-content;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 1.25rem;
}

.main-header-wrapper {
    width: 80%;
    height: 3.125rem;
    border-radius: 0.875rem;
    background-color: var(--color-text-rgb);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 0.625rem;
}

.logo-wrapper {
    height: 90%;
    aspect-ratio: 1;
}

.logo {
    height: 100%;
    width: 100%;
    background-repeat: no-repeat;
    background-image: var(--logo);
    background-size: cover;
    background-position: center;
}

.nav-links {
    height: 100%;
    display: flex;
    align-items: center;
    gap: 0.9375rem;
}

.nav-link {
    text-decoration: none;
    color: var(--vt-c-red);
    letter-spacing: -0.5px;
}

.cta-button {
    height: 85% !important;
    padding-inline: 0.625rem;
    background-color: var(--vt-c-red);
    border-radius: 0.65625rem;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    color: var(--vt-c-white);
    margin-right: calc((3.125rem - (0.85 * 3.125rem)) / 2);
}

@media only screen and (max-width: 768px) {
    .main-header-wrapper {
        position: relative;
    }

    .nav-links {
        position: absolute;
        height: fit-content;
        width: 100%;
        flex-direction: column;
        border: 2px solid black;
        left: 0;
        top: 0;
        padding: 3.125rem 1.25rem 1.25rem 1.25rem;
        border-radius: 0.875rem;
        background-color: var(--vt-c-red-rgb-30);
    }

    .nav-link {
        color: var(--vt-c-white);
        font-size: 1.125rem;
    }

    .cta-button {
        background-color: var(--vt-c-white);
        color: var(--vt-c-red);
        width: 100%;
        height: 3.125rem !important;
        font-size: 1.125rem;
        font-weight: 500;
    }

    .menu-icon,
    .close-icon {
        margin-right: 0.625rem;
        height: 75%;
        aspect-ratio: 1;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
    }

    .menu-icon {
        background-image: url("/images/burger-bar.png");
    }

    .close-icon {
        height: 1.875rem;
        position: absolute;
        right: 0;
        top: 0.625rem;
        background-image: url("/images/close.png");
    }
}
</style>

<script setup>
const paths = [
    {
        name: "Contact",
        path: "/contact",
    },
];
</script>

<template>
    <div class="header-container">
        <div class="main-header-wrapper">
            <RouterLink to="/" class="logo-wrapper">
                <div class="logo"></div>
            </RouterLink>
            <div class="nav-links">
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
</style>

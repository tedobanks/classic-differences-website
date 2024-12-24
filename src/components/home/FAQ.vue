<template>
    <div class="container"></div>
</template>

<style scoped>
.container {
    background: var(--color-text);
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
}

.container::after {
    content: "";
    position: absolute;
    width: 80%;
    aspect-ratio: 1204/424;
    background-color: var(--vt-c-red-dark);
    border-radius: calc(35rem / 16);
    bottom: -100%;
    left: 50%;
    transform: translate(-50%, -125%);
}
</style>

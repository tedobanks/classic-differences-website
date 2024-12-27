<script setup>
import faq from "@/data/faq.json";
import { ref, onMounted } from "vue";

const faqList = ref(faq);

const states = ref([]);

onMounted(() => {
    states.value = Array.from(
        { length: faqList.value.length },
        (_, index) => false
    );
    console.log("Dropdown Toggle states: ", states.value);
});

const toggleDropDown = (index) => {
    states.value[index] = !states.value[index];

    // Set other states to false
    for (let i = 0; i < states.value.length; i++) {
        if (i !== index) {
            states.value[i] = false;
        }
    }

     console.log(states.value)
};
</script>

<template>
    <div class="container" id="faq">
        <h2 class="section-title">FAQ's</h2>
        <p class="description">Providing answers to your questions</p>
        <div class="faq-container">
            <div v-for="(item, index) in faqList" :key="index" class="faq-item">
                <div class="question">
                    <div class="question-text-container">
                        <h5 class="question-text">{{ item.question }}</h5>
                    </div>
                    <div class="accordion-button-container">
                        <button
                            @click="toggleDropDown(index)"
                            class="accordion-button"
                        >
                            <img src="/images/caret.svg" alt="" />
                        </button>
                    </div>
                </div>
                <div v-if="states[index] == true" class="answer">
                    {{ item.answer }}
                </div>
            </div>
        </div>
    </div>
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

.section-title {
    color: var(--color-text-secondary);
    font-weight: 700;
    font-size: 3rem;
    letter-spacing: -3.5px;
    text-transform: none;
    margin-top: 3.125rem;
}

.description {
    color: rgba(0, 0, 0, 0.6);
    text-align: center;
    margin-top: 0.625rem;
}

.faq-container {
    width: 38%;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
    margin-top: 2.5rem;
    margin-bottom: 31.8%;
}

.faq-item {
    width: 100%;
    border-radius: calc(20rem / 16);
    padding-inline: 1.25rem;
    padding-block: 0.9375rem;
    background-color: var(--vt-c-black);
    display: flex;
    flex-direction: column;
}

.question {
    width: 100%;
    display: flex;
    align-items: center;
}

.question-text-container {
    width: 90%;
    padding-right: 0.625rem;
}

.question-text {
    font-size: 1.125rem;
    font-weight: 500;
}

.accordion-button-container {
    width: 10%;
}

.accordion-button {
    width: 100%;
    aspect-ratio: 1;
    background-color: var(--vt-c-red);
    border-radius: 50%;
    border: none;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
}

.accordion-button img {
    width: 30%;
    transform: rotate(270deg);
}

.answer {
    padding-top: 1.25rem;
}

@media only screen and (max-width: 768px) {
    .container {
        padding-inline: 1.25rem;
    }

    .faq-container {
        width: 100%;
    }
}
</style>

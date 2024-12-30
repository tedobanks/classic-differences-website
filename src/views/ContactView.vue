<script setup>
import { ref } from "vue";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const subject = ref("");
const message = ref("");
</script>

<template>
    <div class="container">
        <div class="section-title">Contact Us</div>
        <form
            action="https://formsubmit.co/classicdifferenceslimited@gmail.com"
            method="POST"
        >
            <!-- Redirect route after submission -->
            <input
                type="hidden"
                name="_next"
                value="https://www.classicdifferences.com"
            />
            <!-- Website submission subject -->
            <input type="hidden" name="_subject" value="Website submission!" />
            <!-- reCAPTCHA -->
            <input type="hidden" name="_captcha" value="false" />

            <!-- Actual fields -->
            <div class="inline-input-container">
                <input name="firstname" type="text" placeholder="John" />
                <input name="lastname" type="text" placeholder="Doe" />
            </div>
            <input name="email" type="email" placeholder="abc@example.com" />
            <input name="subject" type="text" placeholder="Subject" />
            <textarea
                name="message"
                id="message"
                cols="30"
                rows="10"
                placeholder="Message"
            ></textarea>
            <div class="submit-container">
                <div class="reply-guarantee-container">
                    <p>
                        We will answer your questions via email within 48 hours.
                    </p>
                </div>
                <button class="submit" type="submit">Send</button>
            </div>
        </form>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    position: relative;
}

.container::before {
    content: "";
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    width: 40rem;
    aspect-ratio: 416/309;
    background-color: var(--vt-c-red);
    border-radius: 50%;
    opacity: 0.5;
    filter: blur(148px);
    z-index: -10;
}

.section-title {
    color: var(--color-text-secondary);
    font-weight: 700;
    font-size: 3rem;
    letter-spacing: -3.5px;
    text-transform: none;
    margin-top: 3.125rem;
}

form {
    width: 50%;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
    margin-top: 2.5rem;
    margin-bottom: 31.8%;
}

input,
textarea {
    width: 100%;
    border: none;
    padding-inline: 0.9375rem;
    border-radius: 0.875rem;
    font-family: "Outfit", serif;
    font-optical-sizing: auto;
    font-size: 15px;
    outline: 0;
}

input {
    height: 3.125rem;
}

textarea {
    resize: none;
    padding-block: 0.625rem;
}

.inline-input-container,
.submit-container {
    width: 100%;
    display: flex;
}

.inline-input-container {
    justify-content: center;
    align-items: center;
    gap: 0.625rem;
}

.submit-container {
    justify-content: space-between;
    align-items: start;
}

.reply-guarantee-container {
    width: 50%;
    padding-left: 0.625rem;
}

.reply-guarantee-container p {
    font-weight: 400;
    font-size: 0.875rem;
    color: var(--color-text);
    opacity: 0.6;
}

.submit {
    height: 3rem;
    width: 8.75rem;
    background-color: var(--vt-c-red);
    color: var(--vt-c-white);
    border-radius: 1.875rem;
    font-family: "Outfit", serif;
    font-optical-sizing: auto;
    font-size: 1rem;
    font-weight: 600;
    border: none;
}

@media only screen and (max-width: 768px) {
    .container {
        overflow: hidden ;
        padding-inline: 1.25rem;
    }

    .container::before {
        top: 50%;
        transform: translate(-50%, -50%);
    }

    form, .submit, .reply-guarantee-container {
        width: 100% !important;
    }

    .inline-input-container,
    .submit-container {
        flex-direction: column;
    }

    .submit-container {
        gap: 0.625rem;
    }
}
</style>

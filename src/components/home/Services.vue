<script setup>
import Service from './widgets/Service.vue';

const displayEvents = [
    "Full-service event planning",
    "Event design and decor",
    "Venue selection and management",
    "Vendor coordination",
    "Budget management",
    "On-site event management",
    "Corporate events",
    "Conferences and meetings",
    "Product launches",
    "Fundraisers",
    "Weddings",
    "Private parties",
    "Event marketing and promotion",
    "Event staffing",
    "Entertainment booking",
    "Catering",
];

const services = [
    {
        imageUrl: "/images/event-planning.jpg",
        name: "Event Planning",
        description:
            "Our expert event planning services cover every aspect of your special occasion, from weddings and anniversaries to birthdays and corporate functions. We handle all logistics, including vendor coordination, budgeting, and day-of execution, ensuring that your event runs seamlessly and exceeds expectations. With a focus on detail and personalized service, we bring your vision to life, allowing you to enjoy your event without the stress of planning.",
    },
    {
        imageUrl: "/images/coverage.jpg",
        name: "Video and Picture Coverage",
        description:
            "Capture the unforgettable moments of your event with our professional video and photography services. Whether it’s a wedding, anniversary, or corporate event, we provide top-tier coverage that reflects the essence of the occasion. Our team focuses on both candid and posed shots to ensure a comprehensive visual record, allowing you to relive the day through high-quality images and films that truly tell the story of your event.",
    },
    {
        imageUrl: "/images/care.jpg",
        name: "Care Home Services",
        description:
            "We offer comprehensive care home solutions, providing cover staff for when you need extra hands, regular maintenance services to keep the facility running smoothly, and necessary supplies to ensure a comfortable environment. Our team is dedicated to maintaining high standards of care and professionalism, giving you peace of mind knowing that every aspect of the care home is well-managed and fully supported.",
    },
    {
        imageUrl: "/images/decor.jpg",
        name: "Event Décor and Setup",
        description:
            "Enhance the ambiance of your event with our custom décor and setup services. From intimate gatherings to large-scale events, we specialize in transforming venues into beautifully designed spaces that match your theme and vision. Our team works closely with you to create personalized décor elements, including lighting, floral arrangements, and custom setups, ensuring that every detail adds to the overall atmosphere of your event.",
    },
];
</script>

<template>
    <div class="container" id="services">
        <h2 class="section-title">Our services</h2>
        <h3 class="description">We can help you with...</h3>
        <div class="mini-carousel">
            <div
                v-for="(item, index) in displayEvents"
                :key="index"
                class="mini-carousel-item"
            >
                {{ item }}
            </div>
        </div>
        <div class="main-carousel">
            <Service v-for="(service, index) in services" :key="index" :service="service" />
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
}

.section-title {
    color: var(--vt-c-red);
    margin-top: 1.25rem;
}

.description {
    font-size: 3.375rem;
    font-weight: 600;
    line-height: 1;
    margin-top: 1.25rem;
    text-align: center;
}

.mini-carousel {
    width: 90%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 0.625rem;
    margin-top: 1.25rem;
}

.mini-carousel-item {
    height: 3.125rem;
    padding-inline: 1.25rem;
    border-radius: 0.5rem;
    background-color: var(--vt-c-red);
    color: var(--color-text-secondary);
    display: flex;
    justify-content: center;
    align-items: center;
}
.main-carousel {
    width: 100%;
    display: flex;
    flex-direction: column;
}

@media only screen and (max-width: 768px) {
    .container {
        padding-inline: 1.25rem;
    }
    .description {
        font-size: 2rem;
    }

    .mini-carousel {
        width: 100%;
        gap: 0.625rem;
        margin-top: 1.25rem;
    }

    .mini-carousel-item {
        height: 3.125rem;
        padding-inline: 0.625rem;
        font-size: 0.75rem;
    }

    .main-carousel {
        gap: 2.5rem;
        margin-top: 3.125rem;
        position: relative;
    }
}
</style>

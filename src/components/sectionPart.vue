<script setup lang="ts">
import { ref, onMounted } from 'vue';

interface PropsSectionPart {
    title: string;
    sourceImage?: string;
    altImage?: string;
    imageLeft?: boolean;
}

const props = withDefaults(defineProps<PropsSectionPart>(), {
    imageLeft: true
});

const { title, sourceImage, altImage, imageLeft } = props;

const sectionRef = ref<HTMLElement>();
const isVisible = ref(false);

onMounted(() => {
    const observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    isVisible.value = true;
                }
            });
        },
        { threshold: 0.2 }
    );

    if (sectionRef.value) {
        observer.observe(sectionRef.value);
    }
});
</script>
<template>
    <section ref="sectionRef" class="section-part" :class="{ 'visible': isVisible, 'image-right': !imageLeft }">
        <div class="section-wrapper">
            <h2 class="title animate-title">{{ title }}</h2>
            <div class="content-wrapper">
                <img class="image animate-image" :src="sourceImage" :alt="altImage" v-if="sourceImage">
                <div class="slot-content animate-slot">
                    <slot></slot>
                </div>
            </div>
        </div>
        <div class="section-divider"></div>
    </section>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.section-part {
    width: 100%;
    position: relative;

    .section-wrapper {
        padding: 4rem 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .title {
        font-size: clamp(1.75rem, 3.5vw, 2.5rem);
        color: $primary-color;
        text-align: center;
        margin-bottom: 4rem;
        font-weight: 800;
        letter-spacing: -0.02em;
        text-transform: uppercase;
        position: relative;
        opacity: 0;
        transform: translateY(30px);
        transition: all 0.8s ease-out;

        &::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, $primary-color, lighten($primary-color, 20%));
            border-radius: 2px;
        }
    }

    .content-wrapper {
        display: flex;
        gap: 3rem;
        align-items: center;
        flex-wrap: wrap;

        .image {
            flex: 0 0 auto;
            max-width: 600px;
            width: 100%;
            height: auto;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
            opacity: 0;
            transform: translateX(-50px);
            transition: all 0.8s ease-out 0.2s;
        }

        .slot-content {
            flex: 1;
            min-width: 300px;
            opacity: 0;
            transform: translateX(50px);
            transition: all 0.8s ease-out 0.4s;
        }
    }

    .section-divider {
        width: 100%;
        height: 1.2px;
        background-color: rgba(128, 128, 128, 0.26);
        margin-top: 3rem;
        opacity: 0;
        transform: scaleX(0);
        transition: all 0.8s ease-out 0.6s;
    }

    &.visible {
        .title {
            opacity: 1;
            transform: translateY(0);
        }

        .image {
            opacity: 1;
            transform: translateX(0);
        }

        .slot-content {
            opacity: 1;
            transform: translateX(0);
        }

        .section-divider {
            opacity: 1;
            transform: scaleX(1);
        }
    }

    &.image-right {
        .content-wrapper {
            flex-direction: row-reverse;

            .image {
                transform: translateX(50px);
            }

            .slot-content {
                transform: translateX(-50px);
            }
        }

        &.visible {
            .image {
                transform: translateX(0);
            }

            .slot-content {
                transform: translateX(0);
            }
        }

        // Responsive pour image-right
        @media (max-width: 768px) {
            .content-wrapper {
                flex-direction: column;

                .image,
                .slot-content {
                    transform: translateY(30px);
                }
            }

            &.visible {

                .image,
                .slot-content {
                    transform: translateY(0);
                }
            }
        }
    }

    // Responsive design
    @media (max-width: 768px) {
        .section-wrapper {
            padding: 2rem 1rem;
        }

        .title {
            font-size: clamp(1.4rem, 5vw, 2rem);
            margin-bottom: 2rem;
            letter-spacing: -0.01em;

            &::after {
                width: 50px;
                height: 2px;
            }
        }

        .content-wrapper {
            flex-direction: column;
            gap: 2rem;
            align-items: center;

            .image {
                max-width: 100%;
                transform: translateY(30px);
            }

            .slot-content {
                transform: translateY(30px);
            }
        }

        &.visible {

            .image,
            .slot-content {
                transform: translateY(0);
            }
        }
    }

    @media (max-width: 480px) {
        .section-wrapper {
            padding: 1.5rem 1rem;
        }

        .content-wrapper {
            gap: 1.5rem;
        }
    }
}
</style>
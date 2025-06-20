<script setup lang="ts">
import SectionPart from "../sectionPart.vue"

//script a placer ici 
</script>

<template>
    <SectionPart title="Un pas vers demain">
        <template #default>
            <div class="contact-content">
                <div class="intro-text">
                    <p class="main-message">
                        Les <strong>Jeux de 2030</strong> ne seront pas l'œuvre d'une personne, mais d'une <em>énergie
                            collective</em>.
                        Si vous êtes à la recherche d'un partenaire engagé, aligné avec l'ambition de ce projet…
                    </p>
                </div>

                <div class="call-to-action">
                    <div class="highlight-box">
                        <p class="statement">
                            <span class="emphasis">Je suis là.</span><br>
                            Ancré dans mes montagnes, tourné vers l'avenir.<br>
                            <strong>Prêt à avancer à vos côtés.</strong>
                        </p>
                    </div>

                    <div class="action-section">
                        <h4 class="action-title">👥 Contactez-moi. Échangeons. Construisons.</h4>

                        <div class="contact-buttons">
                            <a href="mailto:pierregamen@gmail.com" class="btn-primary">
                                <span class="btn-icon">💬</span>
                                <span class="btn-text">Échanger maintenant</span>
                            </a>

                            <div class="contact-info">
                                <div class="info-item">
                                    <span class="info-icon">📧</span>
                                    <span class="info-text">pierregamen@gmail.com</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-icon">📍</span>
                                    <span class="info-text">Région Alpine, France</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-icon">💼</span>
                                    <span class="info-text">Développeur • Manager • Visionnaire</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="closing-message">
                    <p class="vision-text">
                        <em>"Ensemble, transformons les défis olympiques en opportunités durables pour notre territoire
                            et notre avenir."</em>
                    </p>
                </div>
            </div>
        </template>
    </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.contact-content {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: clamp(2rem, 4vw, 3rem);
}

.intro-text {
    .section-subtitle {
        font-size: clamp(1.3rem, 3vw, 1.6rem);
        font-weight: 600;
        color: $primary-color;
        margin: 0 0 1rem 0;
        text-transform: uppercase;
        letter-spacing: 0.5px;
        position: relative;

        &::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, $primary-color 0%, transparent 100%);
            border-radius: 2px;
        }
    }

    .main-message {
        font-size: clamp(1.1rem, 2.5vw, 1.3rem);
        line-height: 1.7;
        color: #333;
        margin: 0;
        text-align: justify;

        strong {
            color: $primary-color;
            font-weight: 700;
        }

        em {
            color: rgba($primary-color, 0.8);
            font-style: italic;
            font-weight: 500;
        }
    }
}

.call-to-action {
    display: flex;
    flex-direction: column;
    gap: clamp(1.5rem, 3vw, 2rem);
}

.highlight-box {
    padding: clamp(1.5rem, 3vw, 2rem);
    background: linear-gradient(135deg,
            rgba($primary-color, 0.08) 0%,
            rgba($primary-color, 0.03) 100%);
    border-radius: 16px;
    border: 2px solid rgba($primary-color, 0.15);
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: linear-gradient(45deg,
                transparent 0%,
                rgba($primary-color, 0.02) 50%,
                transparent 100%);
        animation: shimmer 3s ease-in-out infinite;
    }

    .statement {
        margin: 0;
        font-size: clamp(1.2rem, 2.8vw, 1.5rem);
        line-height: 1.6;
        text-align: center;
        color: #333;

        .emphasis {
            font-size: 1.2em;
            font-weight: 700;
            color: $primary-color;
            display: inline-block;
            margin-bottom: 0.25rem;
        }

        strong {
            color: $primary-color;
            font-weight: 600;
        }
    }
}

.action-section {
    .action-title {
        font-size: clamp(1.2rem, 2.6vw, 1.4rem);
        font-weight: 600;
        color: #555;
        margin: 0 0 1.5rem 0;
        text-align: center;
    }
}

.contact-buttons {
    display: flex;
    flex-direction: column;
    gap: clamp(1.5rem, 3vw, 2rem);
    align-items: center;
}

.btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 0.75rem;
    padding: clamp(1rem, 2.5vw, 1.25rem) clamp(2rem, 4vw, 2.5rem);
    background: linear-gradient(135deg, $primary-color 0%, darken($primary-color, 10%) 100%);
    color: white;
    text-decoration: none;
    border-radius: 50px;
    font-weight: 600;
    font-size: clamp(1.1rem, 2.2vw, 1.25rem);
    box-shadow:
        0 4px 20px rgba($primary-color, 0.3),
        0 2px 8px rgba($primary-color, 0.2);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: linear-gradient(90deg,
                transparent 0%,
                rgba(255, 255, 255, 0.2) 50%,
                transparent 100%);
        transition: left 0.6s ease;
    }

    &:hover {
        transform: translateY(-2px) scale(1.02);
        box-shadow:
            0 8px 30px rgba($primary-color, 0.4),
            0 4px 12px rgba($primary-color, 0.3);

        &::before {
            left: 100%;
        }
    }

    &:active {
        transform: translateY(0) scale(0.98);
    }

    .btn-icon {
        font-size: 1.2em;
    }

    .btn-text {
        white-space: nowrap;
    }
}

.contact-info {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    width: 100%;
    max-width: 400px;
}

.info-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 0.75rem 1rem;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 12px;
    border: 1px solid rgba($primary-color, 0.1);
    transition: all 0.3s ease;

    &:hover {
        background: rgba(255, 255, 255, 0.8);
        border-color: rgba($primary-color, 0.2);
        transform: translateX(4px);
    }

    .info-icon {
        font-size: 1.2rem;
        width: 24px;
        text-align: center;
        flex-shrink: 0;
    }

    .info-text {
        font-size: clamp(0.9rem, 2vw, 1rem);
        color: #555;
        font-weight: 500;
    }
}

.closing-message {
    margin-top: clamp(1rem, 2vw, 1.5rem);

    .vision-text {
        font-size: clamp(1rem, 2.2vw, 1.2rem);
        line-height: 1.6;
        text-align: center;
        margin: 0;
        padding: clamp(1rem, 2.5vw, 1.5rem);
        background: linear-gradient(135deg,
                rgba($primary-color, 0.05) 0%,
                rgba($primary-color, 0.02) 100%);
        border-radius: 12px;
        border-left: 4px solid rgba($primary-color, 0.3);

        em {
            color: #666;
            font-style: italic;
            font-weight: 500;
        }
    }
}

// Animation shimmer
@keyframes shimmer {

    0%,
    100% {
        transform: translateX(-100%);
        opacity: 0;
    }

    50% {
        transform: translateX(0);
        opacity: 1;
    }
}

// Responsive
@media (max-width: 768px) {
    .contact-content {
        gap: 1.5rem;
    }

    .highlight-box {
        padding: 1.5rem;

        .statement {
            text-align: left;
        }
    }

    .contact-info {
        max-width: 100%;
    }

    .info-item {
        padding: 1rem;

        &:hover {
            transform: none;
        }
    }
}

@media (max-width: 480px) {
    .btn-primary {
        width: 100%;
        justify-content: center;

        .btn-text {
            white-space: normal;
            text-align: center;
        }
    }

    .info-item {
        flex-direction: column;
        text-align: center;
        gap: 0.5rem;

        .info-icon {
            width: auto;
        }
    }
}
</style>

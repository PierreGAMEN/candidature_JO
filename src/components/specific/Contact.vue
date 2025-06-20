<script setup lang="ts">
import SectionPart from "../sectionPart.vue"

//script a placer ici 
</script>

<template>
    <SectionPart title="Prêt à construire l’avenir des Jeux 2030, ensemble">
        <template #default>
            <div class="contact-content">
                <div class="intro-text">
                    <p class="main-message">
                        Je suis convaincu que la réussite passera par des femmes et des hommes engagés, fiables et
                        agiles.
                        Si vous cherchez un partenaire qui conjugue expérience, valeurs et esprit d’équipe : je suis là.
                        Ancré dans mes montagnes, tourné vers l’avenir.
                        Prêt à contribuer pleinement à cette aventure.
                    </p>
                </div>

                <div class="call-to-action">


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
                        <em>Ensemble, transformons les défis olympiques en opportunités durables pour notre territoire
                            et notre avenir.</em>
                    </p>
                </div>
            </div>
        </template>
    </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.contact-content {
    margin: 0 auto;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: clamp(2.5rem, 5vw, 4rem);
}

.intro-text {
    text-align: center;

    .main-message {
        font-size: clamp(1.1rem, 2.2vw, 1.3rem);
        line-height: 1.8;
        color: #2c3e50;
        margin: 0;
        margin: 0 auto;
        font-weight: 400;
        letter-spacing: 0.01em;
    }
}

.call-to-action {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: clamp(2rem, 4vw, 3rem);
}

.action-section {
    text-align: center;
    width: 100%;

    .action-title {
        font-size: clamp(1.3rem, 2.5vw, 1.6rem);
        font-weight: 600;
        color: #2c3e50;
        margin: 0 0 clamp(2rem, 3vw, 2.5rem) 0;
        position: relative;

        &::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background: $primary-color;
            border-radius: 2px;
        }
    }
}

.contact-buttons {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: clamp(2rem, 3vw, 2.5rem);
    width: 100%;
}

.btn-primary {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.75rem;
    padding: clamp(1rem, 2.2vw, 1.2rem) clamp(2rem, 4vw, 2.8rem);
    background: $primary-color;
    color: white;
    text-decoration: none;
    border-radius: 8px;
    font-weight: 600;
    font-size: clamp(1rem, 2vw, 1.1rem);
    box-shadow: 0 2px 8px rgba($primary-color, 0.2);
    transition: all 0.2s ease;
    position: relative;
    border: 2px solid $primary-color;

    &:hover {
        background: white;
        color: $primary-color;
        transform: translateY(-1px);
        box-shadow: 0 4px 16px rgba($primary-color, 0.25);
    }

    &:active {
        transform: translateY(0);
    }

    .btn-icon {
        font-size: 1.1em;
    }

    .btn-text {
        font-weight: 600;
        letter-spacing: 0.01em;
    }
}

.contact-info {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1rem;
    width: 100%;
    max-width: 600px;
}

.info-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 1.25rem;
    background: white;
    border-radius: 8px;
    border: 1px solid #e2e8f0;
    transition: all 0.2s ease;

    &:hover {
        border-color: rgba($primary-color, 0.3);
        box-shadow: 0 2px 8px rgba($primary-color, 0.1);
    }

    .info-icon {
        font-size: 1.1rem;
        width: 20px;
        text-align: center;
        flex-shrink: 0;
        color: #64748b;
    }

    .info-text {
        font-size: clamp(0.9rem, 1.8vw, 1rem);
        color: #475569;
        font-weight: 500;
    }
}

.closing-message {
    text-align: center;
    margin-top: clamp(1rem, 2vw, 2rem);

    .vision-text {
        font-size: clamp(1rem, 2vw, 1.15rem);
        line-height: 1.7;
        margin: 0;
        padding: clamp(1.5rem, 3vw, 2rem);
        background: #f8fafc;
        border-radius: 12px;
        border-left: 4px solid $primary-color;
        max-width: 700px;
        margin: 0 auto;

        em {
            color: #64748b;
            font-style: italic;
            font-weight: 500;
        }
    }
}

// Animations d'entrée
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.intro-text {
    animation: fadeInUp 0.6s ease-out;
}

.action-section {
    animation: fadeInUp 0.6s ease-out 0.1s;
    animation-fill-mode: both;
}

.contact-info {
    animation: fadeInUp 0.6s ease-out 0.2s;
    animation-fill-mode: both;
}

.closing-message {
    animation: fadeInUp 0.6s ease-out 0.3s;
    animation-fill-mode: both;
}

// Responsive Design
@media (max-width: 768px) {
    .contact-content {
        gap: 2rem;
    }

    .contact-info {
        grid-template-columns: 1fr;
        max-width: 100%;
    }

    .info-item {
        justify-content: center;
        text-align: center;
    }
}

@media (max-width: 480px) {
    .btn-primary {
        width: 100%;
        max-width: 320px;
    }

    .info-item {
        flex-direction: column;
        gap: 0.5rem;
        padding: 1.25rem;

        .info-icon {
            width: auto;
        }
    }

    .action-section .action-title {
        &::after {
            width: 40px;
        }
    }
}
</style>

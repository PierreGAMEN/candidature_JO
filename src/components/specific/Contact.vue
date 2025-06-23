<script setup lang="ts">
import SectionPart from "../sectionPart.vue"

// Données de contact
const contactData = {
    email: 'pierre.gamen@gmail.com',
    phone: '0673607777',
    phoneDisplay: '06 73 60 77 77'
}
</script>

<template>
    <SectionPart title="Prêt à construire l’avenir des Jeux 2030, ensemble">
        <template #default>
            <div class="contact-content">
                <div class="intro-text">
                    <p class="main-message">
                        Je suis convaincu que la réussite passera par des <strong>femmes et des hommes engagés, fiables
                            et</strong>
                        agiles.
                        Si vous cherchez un collaborateur qui conjugue expérience, valeurs et esprit d’équipe : je suis là.
                        Ancré dans mes montagnes, tourné vers l’avenir.
                        Prêt à contribuer pleinement à cette aventure.
                    </p>
                    <br />
                    <p class="search-statement">
                        C’est dans des missions mêlant coordination, vision et impact collectif que je serai le plus
                        utile. Mon expérience en encadrement, en gestion de projet, ainsi que mes compétences digitales
                        font de moi un atout pour piloter des équipes et accompagner des dynamiques ambitieuses.
                    </p>
                </div>

                <div class="call-to-action">
                    <div class="action-section">
                        <h4 class="action-title">👥 Contactez-moi. Échangeons. Construisons.</h4>

                        <div class="contact-buttons">
                            <a :href="`mailto:${contactData.email}`" class="btn-primary btn-email">
                                <span class="btn-icon">📧</span>
                                <span class="btn-text">{{ contactData.email }}</span>
                            </a>
                            <a :href="`tel:${contactData.phone}`" class="btn-primary btn-phone">
                                <span class="btn-icon">📞</span>
                                <span class="btn-text">{{ contactData.phoneDisplay }}</span>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="engagement">
                    <blockquote class="blockquote-accent">
                        Ensemble, transformons les défis olympiques en opportunités durables pour notre territoire
                        et notre avenir.
                    </blockquote>
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
    gap: var(--spacing-xl);
}

.engagement {
    margin-top: var(--spacing-lg);
}

.intro-text {
    text-align: center;

    .main-message {
        font-size: clamp(1.1rem, 2.2vw, 1.3rem);
        line-height: 1.8;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-lg) 0;
        font-weight: 400;
        letter-spacing: 0.01em;
    }

    .search-statement {
        font-size: clamp(1rem, 2vw, 1.15rem);
        line-height: 1.7;
        color: var(--text-muted);
        margin: 0;
        padding: var(--spacing-md);
        background: linear-gradient(135deg,
                rgba($primary-color, 0.06) 0%,
                rgba($primary-color, 0.02) 100%);
        border-radius: var(--border-radius);
        border-left: 4px solid $primary-color;
        position: relative;
        font-weight: 500;
        max-width: 750px;
        margin: 0 auto;
    }
}

.call-to-action {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: var(--spacing-xl);
}

.action-section {
    text-align: center;
    width: 100%;

    .action-title {
        font-size: clamp(1.3rem, 2.5vw, 1.6rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-lg) 0;
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
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: var(--spacing-md);
    width: 100%;
}

.btn-primary {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    padding: var(--spacing-sm) var(--spacing-md);
    text-decoration: none;
    border-radius: 8px;
    font-weight: 600;
    font-size: clamp(0.9rem, 1.8vw, 1rem);
    transition: all 0.2s ease;
    position: relative;
    border: 2px solid transparent;
    min-width: 180px;

    .btn-icon {
        font-size: 1.1em;
    }

    .btn-text {
        font-weight: 600;
        letter-spacing: 0.01em;
        white-space: nowrap;
    }

    &:active {
        transform: translateY(0);
    }
}

.btn-email {
    background: $primary-color;
    color: white;
    border-color: $primary-color;
    box-shadow: 0 2px 8px rgba($primary-color, 0.2);

    &:hover {
        background: white;
        color: $primary-color;
        transform: translateY(-1px);
        box-shadow: 0 4px 16px rgba($primary-color, 0.25);
    }
}

.btn-phone {
    background: white;
    color: #059669;
    border-color: #059669;
    box-shadow: 0 2px 8px rgba(#059669, 0.15);

    &:hover {
        background: #059669;
        color: white;
        transform: translateY(-1px);
        box-shadow: 0 4px 16px rgba(#059669, 0.25);
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

.engagement {
    animation: fadeInUp 0.6s ease-out 0.2s;
    animation-fill-mode: both;
}

// Responsive Design
@media (max-width: 768px) {
    .contact-content {
        gap: var(--spacing-lg);
    }

    .contact-buttons {
        flex-direction: column;
        gap: var(--spacing-sm);
    }

    .btn-primary {
        width: 100%;
        max-width: 280px;
        min-width: auto;
    }
}

@media (max-width: 480px) {
    .btn-primary {
        width: 100%;
        max-width: 100%;
        padding: var(--spacing-sm) var(--spacing-md);

        .btn-text {
            white-space: normal;
            text-align: center;
        }
    }

    .action-section .action-title {
        &::after {
            width: 40px;
        }
    }
}
</style>

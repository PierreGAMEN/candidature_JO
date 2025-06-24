<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>

<template>
    <SectionPart title="Pourquoi moi pour accompagner les JO 2030 ?">
        <template #default>
            <div class="motivation-content">
                <div class="intro-section">
                    <p class="intro-text">
                        Les <strong>JO d'hiver 2030</strong> dans les Alpes nécessitent
                        <em>excellence opérationnelle</em>, <em>innovation</em> et <em>ancrage territorial</em>.
                        Mon profil peut contribuer à ces enjeux.
                    </p>
                </div>

                <div class="arguments-section">
                    <div class="argument-card featured">
                        <div class="arg-icon">🏔️</div>
                        <div class="arg-content">
                            <h3>Ancrage territorial</h3>
                            <p>
                                <strong>Né et élevé dans les Alpes</strong>, je connais ce territoire,
                                ses spécificités et ses atouts. Une connaissance du terrain essentielle
                                pour organiser des Jeux qui respectent l'identité alpine.
                            </p>
                        </div>
                    </div>

                    <div class="argument-card featured">
                        <div class="arg-icon">🎯</div>
                        <div class="arg-content">
                            <h3>Double expertise</h3>
                            <p>
                                <strong>Management d'équipes</strong> (8 ans) et <strong>développement
                                    numérique</strong> :
                                une combinaison qui permet d'appréhender les JO sous l'angle humain ET technique.
                            </p>
                        </div>
                    </div>

                    <div class="argument-card featured">
                        <div class="arg-icon">🏆</div>
                        <div class="arg-content">
                            <h3>Légitimité sportive</h3>
                            <p>
                                Pratique de <strong>sports olympiques d'hiver</strong> depuis l'enfance,
                                expérience en compétition : je comprends les enjeux des athlètes
                                et partage l'esprit olympique.
                            </p>
                        </div>
                    </div>
                </div>

                <div class="synthese-section">
                    <div class="synthese-content">
                        <blockquote class="synthese-quote">
                            <strong>Ancrage alpin</strong>, <strong>expertise managériale et technique</strong>,
                            <strong>légitimité sportive</strong> : une convergence au service des
                            <em>Jeux Olympiques d'hiver 2030</em>.
                        </blockquote>
                    </div>
                </div>
            </div>
        </template>
    </SectionPart>
</template>

<style scoped lang="scss">
@use '@/styles/variables' as *;

* {
    box-sizing: border-box;
}

.motivation-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
    width: 100%;
    overflow-x: hidden;
}

.intro-section {
    text-align: center;
    margin-bottom: var(--spacing-xl);
}

.intro-text {
    font-size: clamp(1.1rem, 2.5vw, 1.3rem);
    line-height: 1.7;
    color: var(--text-primary);
    margin: 0;
    max-width: 900px;
    margin: 0 auto;

    strong {
        font-weight: 600;
        color: var(--text-primary);
    }

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 500;
    }
}

.arguments-section {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
    gap: var(--spacing-lg);
    margin: var(--spacing-xl) 0;
    width: 100%;
    overflow: hidden;
}

.argument-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    padding: var(--spacing-xl);
    border: 1px solid rgba(0, 0, 0, 0.08);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 3px;
        background: linear-gradient(90deg, rgba($primary-color, 0.6), rgba($primary-color, 0.3));
        transition: var(--transition);
    }

    &.featured {
        border: 2px solid rgba($primary-color, 0.2);
        background: linear-gradient(135deg, rgba($primary-color, 0.05), rgba(255, 255, 255, 0.98));

        &::before {
            height: 4px;
            background: linear-gradient(90deg, $primary-color, lighten($primary-color, 15%));
        }

        .arg-icon {
            background: linear-gradient(135deg, rgba($primary-color, 0.15), rgba($primary-color, 0.08));
            border: 2px solid rgba($primary-color, 0.3);
            transform: scale(1.05);
        }

        .arg-content h3 {
            color: $primary-color;
        }
    }

    &:hover {
        transform: translateY(-3px);
        box-shadow: 0 12px 25px rgba(0, 0, 0, 0.12);

        &::before {
            height: 5px;
        }

        .arg-icon {
            transform: scale(1.1);
        }
    }

    .arg-icon {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 2rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        margin-bottom: var(--spacing-lg);
        transition: all 0.3s ease;
    }

    .arg-content {
        h3 {
            font-size: clamp(1.2rem, 2.5vw, 1.5rem);
            font-weight: 600;
            color: var(--text-primary);
            margin: 0 0 var(--spacing-md) 0;
            line-height: 1.3;
        }

        p {
            font-size: clamp(1rem, 1.8vw, 1.1rem);
            line-height: 1.7;
            color: var(--text-secondary);
            margin: 0 0 var(--spacing-md) 0;

            strong {
                font-weight: 500;
                color: var(--text-primary);
            }
        }
    }
}

.synthese-section {
    margin-top: var(--spacing-xl);
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.08), rgba($primary-color, 0.03));
    border-radius: var(--border-radius-lg);
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
        animation: shimmer 4s ease-in-out infinite;
    }

    .synthese-content {
        position: relative;
        z-index: 1;
        text-align: center;

        h3 {
            font-size: clamp(1.4rem, 2.8vw, 1.8rem);
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
}

.synthese-quote {
    font-size: clamp(1.1rem, 2.5vw, 1.4rem);
    line-height: 1.7;
    color: var(--text-primary);
    font-weight: 300;
    font-style: italic;
    margin: 0 0 var(--spacing-lg) 0;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;

    strong {
        font-weight: 600;
        color: var(--text-primary);
    }

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 500;
    }
}

.call-to-action {
    margin-top: var(--spacing-lg);
    padding: var(--spacing-lg);
    background: rgba(255, 255, 255, 0.9);
    border-radius: var(--border-radius);
    border-left: 4px solid $primary-color;

    .cta-text {
        font-size: clamp(1rem, 2.2vw, 1.2rem);
        line-height: 1.6;
        color: var(--text-primary);
        margin: 0;
        font-weight: 500;
    }
}

// Animations
@keyframes shimmer {

    0%,
    100% {
        transform: translateX(-100%);
        opacity: 0;
    }

    50% {
        transform: translateX(100%);
        opacity: 0.3;
    }
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.intro-section {
    animation: fadeInUp 0.6s ease-out;
}

.argument-card {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    &:nth-child(1) {
        animation-delay: 0.2s;
    }

    &:nth-child(2) {
        animation-delay: 0.4s;
    }

    &:nth-child(3) {
        animation-delay: 0.6s;
    }

    &:nth-child(4) {
        animation-delay: 0.8s;
    }

    &:nth-child(5) {
        animation-delay: 1s;
    }

    &:nth-child(6) {
        animation-delay: 1.2s;
    }
}

.synthese-section {
    animation: fadeInUp 0.6s ease-out 1.4s;
    animation-fill-mode: both;
}

// Responsive Design
@media screen and (max-width: 1024px) {
    .arguments-section {
        grid-template-columns: repeat(auto-fit, minmax(min(280px, 100%), 1fr));
        gap: var(--spacing-md);
    }
}

@media screen and (max-width: 768px) {
    .motivation-content {
        padding: 0 var(--spacing-xs);
    }

    .arguments-section {
        grid-template-columns: 1fr;
        gap: var(--spacing-md);
        margin: var(--spacing-lg) 0;
    }

    .argument-card {
        padding: var(--spacing-lg);
        margin: 0;
        width: 100%;
        box-sizing: border-box;

        .arg-icon {
            width: 60px;
            height: 60px;
            font-size: 1.8rem;
        }
    }

    .synthese-section {
        padding: var(--spacing-lg);
        margin: var(--spacing-lg) 0;
    }

    .intro-text {
        font-size: 1.1rem;
        padding: 0 var(--spacing-sm);
    }
}

@media screen and (max-width: 480px) {
    .motivation-content {
        padding: 0 var(--spacing-xs);
        max-width: 100%;
        overflow-x: hidden;
    }

    .intro-section {
        margin-bottom: var(--spacing-lg);
    }

    .intro-text {
        font-size: 1rem;
        line-height: 1.6;
        padding: 0 var(--spacing-xs);
    }

    .arguments-section {
        gap: var(--spacing-sm);
        margin: var(--spacing-md) 0;
    }

    .argument-card {
        padding: var(--spacing-md);
        margin: 0 0 var(--spacing-sm) 0;

        .arg-icon {
            width: 50px;
            height: 50px;
            font-size: 1.5rem;
            margin-bottom: var(--spacing-md);
        }

        .arg-content {
            h3 {
                font-size: 1.1rem;
                margin-bottom: var(--spacing-sm);
            }

            p {
                font-size: 0.95rem;
                line-height: 1.6;
                margin-bottom: var(--spacing-sm);
            }
        }
    }

    .synthese-section {
        padding: var(--spacing-md);
        margin: var(--spacing-md) 0;

        .synthese-content h3 {
            font-size: 1.3rem;
        }
    }

    .synthese-quote {
        font-size: 1rem;
        line-height: 1.6;
    }

    .call-to-action {
        padding: var(--spacing-md);

        .cta-text {
            font-size: 0.95rem;
        }
    }
}
</style>

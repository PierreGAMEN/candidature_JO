<script setup lang="ts">
import SectionPart from '../sectionPart.vue';


</script>
<template>
    <SectionPart title="Mes convictions me guident"> <template #default>
            <div class="values-container">
                <div class="intro-section">
                    <p class="intro-text">
                        Ces valeurs ne sont pas des mots sur papier. Elles sont le socle de mes décisions,
                        le guide de mes actions, <strong>l'essence de ma candidature</strong>.
                    </p>
                </div>

                <div class="values-grid">
                    <div class="value-card excellence">
                        <div class="card-icon">🎯</div>
                        <div class="card-content">
                            <h3>Exigence et excellence</h3>
                            <p>Parce que viser haut est une habitude forgée en montagne.
                                Chaque sommet atteint révèle un nouveau défi à relever.</p>
                            <span class="value-tag">Performance</span>
                        </div>
                    </div>

                    <div class="value-card sustainability">
                        <div class="card-icon">🌱</div>
                        <div class="card-content">
                            <h3>Sobriété et impact durable</h3>
                            <p>Ce qui est essentiel mérite toute notre attention.
                                Les Jeux de 2030 doivent inspirer, pas épuiser.</p>
                            <span class="value-tag">Écologie</span>
                        </div>
                    </div>

                    <div class="value-card teamwork">
                        <div class="card-icon">🤝</div>
                        <div class="card-content">
                            <h3>Esprit d'équipe</h3>
                            <p>On va plus loin ensemble, quand chacun connaît sa force.
                                L'intelligence collective transforme les défis en opportunités.</p>
                            <span class="value-tag">Collaboration</span>
                        </div>
                    </div>

                    <div class="value-card diversity">
                        <div class="card-icon">🌍</div>
                        <div class="card-content">
                            <h3>Diversité et inclusion</h3>
                            <p>Les parcours atypiques sont souvent les plus riches.
                                Chaque différence est une force pour construire l'avenir.</p>
                            <span class="value-tag">Ouverture</span>
                        </div>
                    </div>

                    <div class="value-card local-global">
                        <div class="card-icon">🏔️</div>
                        <div class="card-content">
                            <h3>Ancrage local, vision globale</h3>
                            <p>Je suis attaché à ma terre, mais je travaille pour l'avenir.
                                Les racines alpines nourrissent une ambition mondiale.</p>
                            <span class="value-tag">Territoire</span>
                        </div>
                    </div>

                    <div class="value-card innovation">
                        <div class="card-icon">⚡</div>
                        <div class="card-content">
                            <h3>Innovation et adaptation</h3>
                            <p>L'avenir appartient à ceux qui osent réinventer.
                                Entre tradition montagnarde et révolution numérique.</p>
                            <span class="value-tag">Modernité</span>
                        </div>
                    </div>
                </div>

                <div class="closing-section">
                    <div class="highlight-quote">
                        <p class="quote-text">
                            <em>"Ces valeurs sont mon ADN. Elles guideront chaque décision,
                                chaque projet, chaque partenariat pour faire des Jeux de 2030
                                un événement à la hauteur de nos ambitions."</em>
                        </p>
                    </div>
                </div>
            </div>
        </template>
    </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.values-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
}

.intro-section {
    text-align: center;
    margin-bottom: clamp(2.5rem, 5vw, 4rem);

    .intro-text {
        font-size: clamp(1.2rem, 2.8vw, 1.5rem);
        line-height: 1.6;
        color: #333;
        margin: 0;
        max-width: 700px;
        margin: 0 auto;

        strong {
            color: $primary-color;
            font-weight: 700;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -2px;
                left: 0;
                right: 0;
                height: 2px;
                background: linear-gradient(90deg, $primary-color 0%, transparent 100%);
                opacity: 0.4;
            }
        }
    }
}

.values-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: clamp(1.5rem, 3vw, 2.5rem);
    margin-bottom: clamp(3rem, 5vw, 4rem);
}

.value-card {
    display: flex;
    gap: 1.5rem;
    padding: clamp(1.5rem, 3vw, 2rem);
    background: linear-gradient(135deg,
            rgba(255, 255, 255, 0.9) 0%,
            rgba(255, 255, 255, 0.7) 100%);
    border-radius: 20px;
    border: 1px solid rgba($primary-color, 0.1);
    box-shadow:
        0 4px 20px rgba(0, 0, 0, 0.06),
        0 1px 3px rgba(0, 0, 0, 0.1);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: linear-gradient(135deg,
                transparent 0%,
                rgba($primary-color, 0.02) 50%,
                transparent 100%);
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    &:hover {
        transform: translateY(-8px) scale(1.02);
        box-shadow:
            0 12px 35px rgba(0, 0, 0, 0.12),
            0 4px 15px rgba(0, 0, 0, 0.08);

        &::before {
            opacity: 1;
        }

        .card-icon {
            transform: scale(1.1) rotate(5deg);
        }

        .value-tag {
            transform: translateX(0);
            opacity: 1;
        }
    }

    // Couleurs des anneaux olympiques
    &.excellence {
        border-top: 4px solid #0085C3; // Bleu olympique

        .card-icon {
            background: linear-gradient(135deg, #0085C3, #005A8B);
        }

        .value-tag {
            background: linear-gradient(135deg, #0085C3, #005A8B);
        }
    }

    &.sustainability {
        border-top: 4px solid #00A651; // Vert olympique

        .card-icon {
            background: linear-gradient(135deg, #00A651, #007A3E);
        }

        .value-tag {
            background: linear-gradient(135deg, #00A651, #007A3E);
        }
    }

    &.teamwork {
        border-top: 4px solid #EE334E; // Rouge olympique

        .card-icon {
            background: linear-gradient(135deg, #EE334E, #C41E3A);
        }

        .value-tag {
            background: linear-gradient(135deg, #EE334E, #C41E3A);
        }
    }

    &.diversity {
        border-top: 4px solid #FFD100; // Jaune olympique

        .card-icon {
            background: linear-gradient(135deg, #FFD100, #FFC400);
        }

        .value-tag {
            background: linear-gradient(135deg, #FFD100, #FFC400);
            color: #333; // Texte sombre sur fond jaune
        }
    }

    &.local-global {
        border-top: 4px solid #333333; // Noir olympique (adouci)

        .card-icon {
            background: linear-gradient(135deg, #333333, #1a1a1a);
        }

        .value-tag {
            background: linear-gradient(135deg, #333333, #1a1a1a);
        }
    }

    &.innovation {
        border-top: 4px solid $primary-color; // Couleur primaire du site

        .card-icon {
            background: linear-gradient(135deg, $primary-color, darken($primary-color, 15%));
        }

        .value-tag {
            background: linear-gradient(135deg, $primary-color, darken($primary-color, 15%));
        }
    }
}

.card-icon {
    width: 70px;
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.8rem;
    border-radius: 50%;
    flex-shrink: 0;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.card-content {
    flex: 1;
    position: relative;

    h3 {
        font-size: clamp(1.2rem, 2.4vw, 1.4rem);
        font-weight: 700;
        color: #2c3e50;
        margin: 0 0 0.75rem 0;
        line-height: 1.3;
    }

    p {
        font-size: clamp(1rem, 2vw, 1.1rem);
        line-height: 1.6;
        color: #555;
        margin: 0 0 1rem 0;
        text-align: justify;
    }
}

.value-tag {
    display: inline-block;
    padding: 0.4rem 1rem;
    border-radius: 20px;
    color: white;
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    transform: translateX(-10px);
    opacity: 0;
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.closing-section {
    margin-top: clamp(2rem, 4vw, 3rem);
}

.highlight-quote {
    text-align: center;
    padding: clamp(2rem, 4vw, 3rem);
    background: linear-gradient(135deg,
            rgba($primary-color, 0.08) 0%,
            rgba($primary-color, 0.03) 100%);
    border-radius: 24px;
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

    .quote-text {
        font-size: clamp(1.1rem, 2.5vw, 1.3rem);
        line-height: 1.7;
        margin: 0;
        color: #2c3e50;
        max-width: 800px;
        margin: 0 auto;
        position: relative;
        z-index: 1;

        em {
            font-style: italic;
            position: relative;

            &::before,
            &::after {
                content: '"';
                font-size: 1.5em;
                color: rgba($primary-color, 0.3);
                font-weight: 300;
                position: absolute;
                top: -0.1em;
            }

            &::before {
                left: -0.5em;
            }

            &::after {
                right: -0.5em;
            }
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
        transform: translateX(100%);
        opacity: 0.3;
    }
}

// Animation d'entrée
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

.value-card {
    animation: fadeInUp 0.6s ease-out;

    &:nth-child(1) {
        animation-delay: 0.1s;
    }

    &:nth-child(2) {
        animation-delay: 0.2s;
    }

    &:nth-child(3) {
        animation-delay: 0.3s;
    }

    &:nth-child(4) {
        animation-delay: 0.4s;
    }

    &:nth-child(5) {
        animation-delay: 0.5s;
    }

    &:nth-child(6) {
        animation-delay: 0.6s;
    }
}

// Responsive
@media (max-width: 768px) {
    .values-grid {
        grid-template-columns: 1fr;
        gap: 1.5rem;
    }

    .value-card {
        flex-direction: column;
        text-align: center;
        gap: 1rem;

        .card-content {
            p {
                text-align: center;
            }
        }

        &:hover {
            transform: translateY(-4px) scale(1.01);
        }
    }

    .card-icon {
        align-self: center;
        width: 60px;
        height: 60px;
        font-size: 1.5rem;
    }

    .highlight-quote {
        .quote-text {
            em {

                &::before,
                &::after {
                    display: none;
                }
            }
        }
    }
}

@media (max-width: 480px) {
    .values-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
    }

    .value-card {
        padding: 1.5rem;
    }

    .card-icon {
        width: 50px;
        height: 50px;
        font-size: 1.3rem;
    }

    .highlight-quote {
        padding: 1.5rem;
    }
}
</style>
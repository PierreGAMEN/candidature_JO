<script setup lang="ts">
import SectionPart from '../sectionPart.vue';


</script>
<template>
    <SectionPart title="Mes forces au service des Jeux">
        <template #default>
            <div class="adventure-content">
                <p class="intro-text">
                    Rejoindre l’organisation des <em>Jeux</em>, c’est mettre en
                    mouvement <strong>ses compétences, ses convictions et son énergie</strong> au service d’un événement
                    porteur de sens.

                </p>
                <div class="motivation-section">
                    <div class="reasons-list">
                        <div class="reason-item">
                            <div class="card-icon">🎯</div>
                            <div class="content">
                                <h4>Approche pragmatique</h4>
                                <p>
                                    Je transforme des ambitions en actions mesurables et efficaces, en m’appuyant sur
                                    mon expérience terrain et mes compétences numériques.
                                </p>
                            </div>
                        </div>

                        <div class="reason-item">
                            <div class="card-icon">🤝</div>
                            <div class="content">
                                <h4>Capacité à fédérer</h4>
                                <p>
                                    Manager comme développeur, je sais fédérer des équipes autour d’un cap clair, dans
                                    un esprit de confiance et d’engagement.
                                </p>
                            </div>
                        </div>

                        <div class="reason-item">
                            <div class="card-icon">⚡</div>
                            <div class="content">
                                <h4>Adaptabilité</h4>
                                <p>
                                    Je m’épanouis dans des environnements exigeants, changeants — en montagne comme dans
                                    le digital — avec rigueur et curiosité.
                                </p>
                            </div>
                        </div>

                        <div class="reason-item">
                            <div class="card-icon">📊</div>
                            <div class="content">
                                <h4>Analyse et prise de recul</h4>
                                <p>
                                    Je sais prendre de la hauteur, lire les signaux clés et décider vite et bien, même
                                    dans l’urgence. Ma force : allier données, écoute et instinct terrain.
                                </p>
                            </div>
                        </div>

                        <div class="reason-item">
                            <div class="card-icon">🚀</div>
                            <div class="content">
                                <h4>Vision durable</h4>
                                <p>
                                    Je crois en une innovation sobre, utile et inclusive, capable d’avoir un impact
                                    positif à long terme pour nos territoires.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- <div class="engagement">
                    <blockquote>
                        Mon engagement : mettre mon expérience au service de Jeux exemplaires,
                        ancrés dans leur territoire et tournés vers l'avenir.
                    </blockquote>
                </div> -->
            </div>
        </template>
    </SectionPart>

</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.adventure-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
}

.intro-text {
    font-size: clamp(1.1rem, 2.5vw, 1.25rem);
    line-height: 1.8;
    color: #2d3748;
    margin-bottom: var(--spacing-lg);
    font-weight: 400;
    letter-spacing: 0.01em;

    strong {
        color: $primary-color;
        font-weight: 600;
        background: linear-gradient(120deg, transparent 0%, rgba($primary-color, 0.1) 0%);
        padding: 0.1em 0.2em;
        border-radius: 4px;
    }

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 600;
        position: relative;

        &::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, $primary-color, lighten($primary-color, 20%));
            border-radius: 1px;
        }
    }
}

.motivation-section {
    margin: clamp(2rem, 4vw, 3rem) 0;
}

.reasons-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: clamp(1.5rem, 3vw, 2rem);
    margin-bottom: clamp(2rem, 4vw, 3rem);
}

.reason-item {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
    padding: clamp(1.5rem, 3vw, 2rem);
    background: rgba(255, 255, 255, 0.98);
    border-radius: 16px;
    border: 1px solid rgba(0, 0, 0, 0.06);
    border-top: 4px solid transparent;
    transition: all 0.3s ease;
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.04);

    // Touche de couleur subtile par position (bordure gauche uniquement)
    &:nth-child(1) {
        // 🎯 Approche pragmatique - BLEU
        border-top-color: #0085C3;

        .content h4 {
            color: #2c3e50;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #0085C3;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(2) {
        // 🤝 Capacité à fédérer - JAUNE
        border-top-color: #FFD100;

        .content h4 {
            color: #2c3e50;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #FFD100;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(3) {
        // ⚡ Adaptabilité - NOIR
        border-top-color: #333333;

        .content h4 {
            color: #2c3e50;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #333333;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(4) {
        // 🏔️ Engagement local - VERT
        border-top-color: #00A651;

        .content h4 {
            color: #2c3e50;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #00A651;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(5) {
        // 🚀 Vision globale - ROUGE
        border-top-color: #EE334E;

        .content h4 {
            color: #2c3e50;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #EE334E;
                border-radius: 1px;
            }
        }
    }

    &:hover {
        transform: translateY(-4px);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
        border-top-width: 10px;
    }
}

.card-icon {
    width: clamp(60px, 8vw, 70px);
    height: clamp(60px, 8vw, 70px);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: clamp(1.5rem, 2.5vw, 1.8rem);
    background: #f8f9fa;
    color: #6c757d;
    transition: all 0.3s ease;
    border: 1px solid rgba(0, 0, 0, 0.06);

    &:hover {
        transform: scale(1.05);
        background: #f1f3f4;
    }
}

.content {
    text-align: center;
    flex: 1;

    h4 {
        font-size: clamp(1.2rem, 2.5vw, 1.4rem);
        font-weight: 600;
        margin: 0 0 1rem 0;
        line-height: 1.3;
        transition: all 0.3s ease;
    }

    p {
        font-size: clamp(0.9rem, 1.8vw, 1rem);
        line-height: 1.6;
        color: #6c757d;
        margin: 0;
        text-align: left;
    }
}

.engagement {
    margin-top: clamp(3rem, 5vw, 4rem);
    text-align: center;

    blockquote {
        font-size: clamp(1.1rem, 2.5vw, 1.3rem);
        font-style: italic;
        line-height: 1.7;
        color: #2c3e50;
        margin: 0;
        padding: clamp(2rem, 4vw, 3rem);
        background: linear-gradient(135deg,
                rgba($primary-color, 0.08) 0%,
                rgba($primary-color, 0.03) 100%);
        border-radius: 24px;
        border: 2px solid rgba($primary-color, 0.15);
        position: relative;
        overflow: hidden;
        max-width: 800px;
        margin: 0 auto;

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

        &::after {
            content: '"';
            position: absolute;
            top: 15px;
            left: 25px;
            font-size: clamp(2.5rem, 5vw, 3rem);
            color: rgba($primary-color, 0.2);
            font-family: serif;
            line-height: 1;
        }
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
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

// Animation d'entrée séquentielle simplifiée
.reason-item {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    @for $i from 1 through 5 {
        &:nth-child(#{$i}) {
            animation-delay: #{($i - 1) * 0.1}s;
        }
    }
}

// Responsive Design
@media (max-width: 768px) {
    .reasons-list {
        grid-template-columns: 1fr;
        gap: 1.5rem;
    }

    .reason-item {
        padding: 1.5rem;

        &:hover {
            transform: translateY(-4px) scale(1.01);
        }

        .content p {
            text-align: center;
        }
    }

    .card-icon {
        width: 60px;
        height: 60px;
        font-size: 1.5rem;
    }

    .engagement blockquote {
        padding: 1.5rem;

        &::after {
            font-size: 2rem;
            top: 10px;
            left: 15px;
        }
    }
}

@media (max-width: 480px) {
    .reason-item {
        padding: 1.25rem;
        gap: 1rem;
    }

    .card-icon {
        width: 50px;
        height: 50px;
        font-size: 1.3rem;
    }

    .engagement blockquote {
        padding: 1.25rem;

        &::after {
            display: none;
        }
    }
}
</style>
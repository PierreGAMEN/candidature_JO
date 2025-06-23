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
    color: var(--text-primary);
    margin-bottom: var(--spacing-xl);
    font-weight: 400;
    letter-spacing: 0.01em;
    text-align: center;
    position: relative;

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 600;
        position: relative;
        z-index: 1;

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

    strong {
        position: relative;
        z-index: 1;
    }
}

.motivation-section {
    margin: var(--spacing-xl) 0;
}

.reasons-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-lg);
    margin-bottom: var(--spacing-xl);
}

.reason-item {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: var(--spacing-md);
    padding: var(--spacing-lg);
    background: rgba(255, 255, 255, 0.98);
    border-radius: var(--border-radius-lg);
    border: 1px solid rgba(0, 0, 0, 0.06);
    transition: var(--transition);
    box-shadow: var(--shadow-sm);
    overflow: hidden;

    // Anneau olympique décoratif en arrière-plan
    &::before {
        content: '';
        position: absolute;
        top: -20px;
        right: -20px;
        width: 80px;
        height: 80px;
        border-radius: 50%;
        border: 8px solid transparent;
        opacity: 0.2;
        transition: var(--transition);
        z-index: 0;
    }

    // Effet de survol sur l'anneau
    &:hover::before {
        opacity: 0.5;
        transform: scale(1.3);
        top: -25px;
        right: -25px;
    }

    // Couleurs des anneaux olympiques
    &:nth-child(1) {

        // 🎯 Approche pragmatique - BLEU olympique
        &::before {
            border-color: #0085C3;
        }

        .content h4 {
            color: var(--text-primary);
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

        // 🤝 Capacité à fédérer - JAUNE olympique
        &::before {
            border-color: #000000;
        }

        .content h4 {
            color: var(--text-primary);
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: black;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(3) {

        // ⚡ Adaptabilité - NOIR olympique
        &::before {
            border-color: red;
        }

        .content h4 {
            color: var(--text-primary);
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: red;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(4) {

        // 📊 Analyse - VERT olympique
        &::before {
            border-color: yellow;
        }

        .content h4 {
            color: var(--text-primary);
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: yellow;
                border-radius: 1px;
            }
        }
    }

    &:nth-child(5) {

        // 🚀 Vision durable - ROUGE olympique
        &::before {
            border-color: #2e9b33;
        }

        .content h4 {
            color: var(--text-primary);
            position: relative;

            &::after {
                content: '';
                position: absolute;
                bottom: -4px;
                left: 0;
                width: 30px;
                height: 2px;
                background: #2e9b33;
                border-radius: 1px;
            }
        }
    }

    &:hover {
        transform: translateY(-6px);
        box-shadow: var(--shadow-lg);
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
    transition: var(--transition);
    border: 1px solid rgba(0, 0, 0, 0.06);
    position: relative;
    z-index: 2;

    &:hover {
        transform: scale(1.05);
        background: #f1f3f4;
    }
}

.content {
    text-align: center;
    flex: 1;
    position: relative;
    z-index: 1;

    h4 {
        font-size: clamp(1.2rem, 2.5vw, 1.4rem);
        font-weight: 600;
        margin: 0 0 1rem 0;
        line-height: 1.3;
        transition: var(--transition);
    }

    p {
        font-size: clamp(0.9rem, 1.8vw, 1rem);
        line-height: 1.6;
        color: var(--text-secondary);
        margin: 0;
        text-align: left;
    }
}

// Animations
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
        gap: var(--spacing-md);
    }

    .reason-item {
        padding: var(--spacing-md);

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
}

@media (max-width: 480px) {
    .reason-item {
        padding: var(--spacing-sm);
        gap: var(--spacing-sm);
    }

    .card-icon {
        width: 50px;
        height: 50px;
        font-size: 1.3rem;
    }
}
</style>
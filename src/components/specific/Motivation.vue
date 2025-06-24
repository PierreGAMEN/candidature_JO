<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>

<template>
    <SectionPart title="Pourquoi moi pour accompagner les JO 2030 ?">
        <template #default>
            <div class="motivation-content">
                <div class="intro-section">
                    <p class="intro-text">
                        Les <strong>Jeux Olympiques d'hiver 2030</strong> dans les Alpes françaises représentent
                        un défi unique qui nécessite une approche alliant <em>excellence opérationnelle</em>,
                        <em>innovation durable</em> et <em>ancrage territorial</em>.
                        Mon profil peut contribuer à ces enjeux.
                    </p>
                </div>

                <div class="arguments-section">
                    <div class="argument-card featured">
                        <div class="arg-icon">🏔️</div>
                        <div class="arg-content">
                            <h3>Connaissance territoriale</h3>
                            <p>
                                <strong>Né et élevé dans les Alpes</strong>, je connais ce territoire,
                                ses spécificités, ses défis et ses atouts. Cette connaissance du terrain peut être
                                utile pour organiser des Jeux qui respectent et valorisent l'identité alpine.
                            </p>
                            <ul class="argument-points">
                                <li>Connaissance approfondie du territoire alpin</li>
                                <li>Réseau local et compréhension des enjeux régionaux</li>
                                <li>Expérience de la montagne en toutes saisons</li>
                            </ul>
                        </div>
                    </div>

                    <div class="argument-card featured">
                        <div class="arg-icon">🏆</div>
                        <div class="arg-content">
                            <h3>Expérience sportive</h3>
                            <p>
                                Pratiquant de <strong>sports olympiques d'hiver</strong> depuis l'enfance et
                                ayant eu une <strong>expérience en compétition</strong> pendant plusieurs années, je
                                peux comprendre les enjeux
                                des athlètes et partager l'esprit olympique.
                            </p>
                            <ul class="argument-points">
                                <li>Pratique du ski alpin depuis mes 5 ans</li>
                                <li>Expérience en compétition (ski de fond, trail, ski-alpinisme)</li>
                                <li>Compréhension des besoins des athlètes</li>
                            </ul>
                        </div>
                    </div>

                    <div class="argument-card">
                        <div class="arg-icon">💼</div>
                        <div class="arg-content">
                            <h3>Expertise opérationnelle</h3>
                            <p>
                                <strong>8 ans de management</strong> m'ont donné une solide expérience en
                                coordination d'équipes, gestion de projets complexes et amélioration continue.
                            </p>
                            <ul class="argument-points">
                                <li>Management d'équipes de 15 à 20 personnes</li>
                                <li>Pilotage de projets transversaux</li>
                                <li>Expertise en amélioration des processus</li>
                            </ul>
                        </div>
                    </div>

                    <div class="argument-card">
                        <div class="arg-icon">💻</div>
                        <div class="arg-content">
                            <h3>Vision digitale</h3>
                            <p>
                                En tant que <strong>développeur web</strong>, j'apporte une expertise technique
                                moderne, essentielle pour des Jeux innovants et connectés.
                            </p>
                            <ul class="argument-points">
                                <li>Développement de solutions numériques</li>
                                <li>Approche UX/UI centrée utilisateur</li>
                                <li>Compréhension des enjeux technologiques actuels</li>
                            </ul>
                        </div>
                    </div>

                    <div class="argument-card">
                        <div class="arg-icon">🌱</div>
                        <div class="arg-content">
                            <h3>Engagement durable</h3>
                            <p>
                                Passionné de montagne, je suis sensible aux <strong>enjeux environnementaux</strong>
                                et à la nécessité d'organiser des Jeux exemplaires et responsables.
                            </p>
                            <ul class="argument-points">
                                <li>Sensibilité écologique et respect de la montagne</li>
                                <li>Approche durable dans mes projets</li>
                                <li>Vision long terme pour le territoire</li>
                            </ul>
                        </div>
                    </div>

                    <div class="argument-card">
                        <div class="arg-icon">🤝</div>
                        <div class="arg-content">
                            <h3>Esprit collaboratif</h3>
                            <p>
                                Mon expérience en <strong>magasin</strong> et ma pratique sportive
                                m'ont appris l'importance de la collaboration et du dépassement collectif.
                            </p>
                            <ul class="argument-points">
                                <li>Capacité à fédérer et motiver</li>
                                <li>Expérience de la collaboration intersectorielle</li>
                                <li>Esprit de cordée</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="synthese-section">
                    <div class="synthese-content">
                        <h3>Une approche globale</h3>
                        <blockquote class="synthese-quote">
                            Mon profil combine <strong>ancrage territorial</strong>, <strong>légitimité
                                sportive</strong>,
                            <strong>expertise managériale</strong> et <strong>vision technologique</strong>.
                            Cette convergence me permet d'appréhender les Jeux Olympiques sous différents angles :
                            <em>humain</em>, <em>technique</em>, <em>territorial</em> et <em>durable</em>.
                        </blockquote>

                        <div class="call-to-action">
                            <p class="cta-text">
                                Prêt à mettre cette envie et ces expériences au service d'un projet qui marquera
                                l'histoire du sport et du territoire alpin.
                            </p>
                        </div>
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

.argument-points {
    list-style: none;
    padding: 0;
    margin: 0;

    li {
        font-size: clamp(0.9rem, 1.6vw, 1rem);
        color: var(--text-secondary);
        padding: var(--spacing-xs) 0;
        position: relative;
        padding-left: 1.5rem;

        &::before {
            content: '▶';
            color: $primary-color;
            font-size: 0.8rem;
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
        }

        &+li {
            margin-top: var(--spacing-xs);
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

    .argument-points {
        li {
            font-size: 0.9rem;
            padding: var(--spacing-xs) 0;
            padding-left: 1.2rem;

            &::before {
                font-size: 0.7rem;
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

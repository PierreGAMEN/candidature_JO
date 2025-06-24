<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>
<template>
    <SectionPart title="Un sportif engagé pour les Jeux 2030">
        <template #default>
            <div class="sportif-content">
                <div class="intro-section">
                    <p class="intro-quote">
                        « Ayant grandi en montagne, j'ai toujours pratiqué des <strong>sports olympiques
                            d'hiver</strong>.
                        D'abord en loisir, rapidement en <em>compétition</em>. »
                    </p>
                </div>

                <div class="parcours-section">
                    <!-- Compétition de haut niveau -->
                    <div class="parcours-item">
                        <div class="sport-icon">🏆</div>
                        <div class="content">
                            <h3>Compétition</h3>
                            <p>
                                La montagne a toujours été mon terrain de jeu, mais c’est en <strong>trail
                                    running</strong> que j’ai le plus exploré mes limites.
                                Pendant six ans, j’ai couru en compétition, accompagné par un coach personnel.
                                Le <strong>ski-alpinisme</strong> est venu en parallèle, avec des courses emblématiques
                                comme la <em>Pierra Menta</em> ou la <em>TSF Millet</em>.
                                J’ai aussi pratiqué le <strong>ski de fond</strong> en club durant plusieurs années.
                            </p>


                        </div>
                    </div>

                    <!-- Sports olympiques -->
                    <div class="parcours-item">
                        <div class="sport-icon">⛷️</div>
                        <div class="content">
                            <h3>Sports olympiques d’hiver</h3>
                            <p>
                                J’ai grandi avec les disciplines phares des <em>Jeux Olympiques d’hiver</em>.
                                Le <strong>ski alpin</strong> fait partie de mon quotidien depuis l’âge de 4 ans, et
                                j’ai pratiqué le <strong>ski de fond</strong> en club dès mes 10 ans, avec une
                                expérience en compétition.
                                Cette proximité avec les sports d’hiver m’a permis de développer une compréhension fine
                                des exigences, des formats et des valeurs portées par ces disciplines.
                            </p>

                        </div>
                    </div>

                    <!-- Formation technique -->
                    <div class="parcours-item">
                        <div class="sport-icon">🎓</div>
                        <div class="content">
                            <h3>Formation technique</h3>
                            <p>
                                J’ai suivi un cursus unique au lycée de Moûtiers, en <strong>section montagne</strong>
                                pendant 4 ans. Cette formation m’a permis d’acquérir les bases techniques et la culture
                                de la montagne à travers l’alpinisme, le ski de
                                randonnée, l’orientation et l’escalade.
                            </p>
                            <p>
                                J’ai également validé une <strong>formation d’accompagnateur en moyenne
                                    montagne</strong>, renforçant mes compétences en terrain, ma capacité à encadrer et
                                ma connaissance fine de l’environnement alpin.
                            </p>
                        </div>
                    </div> <!-- Pratique assidue -->
                    <div class="parcours-item">
                        <div class="sport-icon">🧗</div>
                        <div class="content">
                            <h3>Le sport au quotidien</h3>
                            <p>
                                Le sport ne se résume pas à un souvenir ou à un palmarès — il <strong>structure encore
                                    aujourd’hui mon quotidien.</strong> Escalade, ski, course en montagne : je pratique
                                régulièrement, toute l’année, avec la même envie d’effort et de progression. Cet
                                engagement constant nourrit mon équilibre, ma rigueur et mon énergie. Il m’ancre dans
                                <strong>une culture de l’action</strong>, que je souhaite mettre au service d’un projet
                                collectif comme
                                les Jeux.
                            </p>

                        </div>
                    </div>

                    <!-- Esprit olympique -->
                    <div class="parcours-item">
                        <div class="sport-icon">🤝</div>
                        <div class="content">
                            <h3>De spectateur à bâtisseur</h3>
                            <p>
                                J’ai <strong>grandi avec les compétitions sportives</strong> : les suivre faisait partie
                                de mes saisons,
                                comme un rendez-vous familier. Aujourd’hui, <strong>je veux passer de l’autre
                                    côté</strong>. Contribuer à
                                l’organisation des Jeux, c’est rendre à ce monde une part de ce qu’il m’a transmis —
                                émotions, repères, exigence.
                            </p>

                        </div>
                    </div>
                </div>

                <div class="conclusion-section">
                    <blockquote class="conclusion-quote">
                        Ce parcours sportif m'a forgé les valeurs olympiques :
                        <strong>excellence, respect, amitié</strong>. Une légitimité terrain pour porter
                        les <em>Jeux Olympiques d'hiver 2030</em> dans les Alpes françaises.
                    </blockquote>
                </div>
            </div>
        </template>
    </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.sportif-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
}

.intro-section {
    margin-bottom: var(--spacing-xl);
    text-align: center;
}

.intro-quote {
    font-size: clamp(1.3rem, 3vw, 1.6rem);
    line-height: 1.6;
    color: var(--text-primary);
    font-weight: 300;
    font-style: italic;
    margin: 0;
    padding: var(--spacing-lg);
    background: linear-gradient(135deg, rgba($primary-color, 0.08), rgba(255, 255, 255, 0.95));
    border-radius: var(--border-radius-lg);
    border-left: 4px solid $primary-color;
    box-shadow: var(--shadow-md);
    position: relative;

    // Anneaux olympiques décoratifs subtils
    &::before {
        content: '';
        position: absolute;
        top: -8px;
        right: 20px;
        width: 60px;
        height: 25px;
        background:
            radial-gradient(circle at 8px 12px, transparent 4px, rgba(0, 133, 195, 0.3) 4px, rgba(0, 133, 195, 0.3) 6px, transparent 6px),
            radial-gradient(circle at 20px 12px, transparent 4px, rgba(51, 51, 51, 0.3) 4px, rgba(51, 51, 51, 0.3) 6px, transparent 6px),
            radial-gradient(circle at 32px 12px, transparent 4px, rgba(238, 51, 78, 0.3) 4px, rgba(238, 51, 78, 0.3) 6px, transparent 6px),
            radial-gradient(circle at 44px 12px, transparent 4px, rgba(255, 209, 0, 0.3) 4px, rgba(255, 209, 0, 0.3) 6px, transparent 6px),
            radial-gradient(circle at 56px 12px, transparent 4px, rgba(0, 166, 81, 0.3) 4px, rgba(0, 166, 81, 0.3) 6px, transparent 6px);
    }

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 500;
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

.parcours-section {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--spacing-xl);
    margin: var(--spacing-xl) 0;

    // 2 colonnes sur desktop et tablette, 1 colonne sur mobile
    @media (max-width: 768px) {
        grid-template-columns: 1fr;
        gap: var(--spacing-lg);
    }
}

.parcours-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: var(--spacing-lg);
    padding: var(--spacing-xl);
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    border: 1px solid rgba(0, 0, 0, 0.08);
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 3px;
        background: linear-gradient(90deg, $primary-color, lighten($primary-color, 20%));
        transition: var(--transition);
    }

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        border-color: rgba($primary-color, 0.2);

        .sport-icon {
            transform: scale(1.05);
            background: linear-gradient(135deg, rgba($primary-color, 0.15), rgba($primary-color, 0.08));
        }
    }

    // Animation d'entrée séquentielle
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    @for $i from 1 through 6 {
        &:nth-child(#{$i}) {
            animation-delay: #{($i - 1) * 0.1}s;
        }
    }
}

.sport-icon {
    width: clamp(60px, 6vw, 70px);
    height: clamp(60px, 6vw, 70px);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: clamp(1.8rem, 2.5vw, 2rem);
    background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
    border: 2px solid rgba($primary-color, 0.15);
    transition: all 0.3s ease;
    flex-shrink: 0;
    margin-bottom: var(--spacing-sm);
}

.content {
    text-align: center;
    width: 100%;

    h3 {
        font-size: clamp(1.2rem, 2.2vw, 1.4rem);
        font-weight: 500;
        margin: 0 0 var(--spacing-md) 0;
        color: var(--text-primary);
        line-height: 1.3;
        position: relative;

        &::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 2px;
            background: $primary-color;
            border-radius: 1px;
        }
    }

    p {
        font-size: clamp(0.95rem, 1.8vw, 1.05rem);
        line-height: 1.7;
        color: var(--text-secondary);
        margin: 0;
        text-align: left;
        max-width: 100%;
        padding: var(--spacing-md) 0 0;

        strong {
            font-weight: 500;
            color: var(--text-primary);
        }

        em {
            color: $primary-color;
            font-style: normal;
            font-weight: 500;
        }

        &+p {
            margin-top: var(--spacing-sm);
        }
    }
}

.conclusion-section {
    margin-top: var(--spacing-xl);
    text-align: center;
    width: 100%;
    display: flex;
    justify-content: center;
}

.conclusion-quote {
    font-size: clamp(1.1rem, 2.5vw, 1.25rem);
    line-height: 1.8;
    color: var(--text-primary);
    font-weight: 400;
    margin: 0;
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
    border-radius: var(--border-radius-lg);
    border: 2px solid rgba($primary-color, 0.2);
    position: relative;
    text-align: center;
    width: 100%;
    max-width: 800px;
    box-sizing: border-box;

    // Médaille olympique décorative
    &::before {
        content: '🏅';
        position: absolute;
        top: -15px;
        left: 50%;
        transform: translateX(-50%);
        font-size: 2rem;
        background: white;
        padding: 5px 10px;
        border-radius: 50%;
        box-shadow: var(--shadow-sm);
    }

    // Barre décorative en bas
    &::after {
        content: '';
        position: absolute;
        bottom: -8px;
        left: 50%;
        transform: translateX(-50%);
        width: 80px;
        height: 4px;
        background: linear-gradient(90deg,
                #0085C3, #333333, #EE334E, #FFD100, #00A651);
        border-radius: 2px;
    }

    em {
        color: $primary-color;
        font-style: normal;
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 0.5px;
    }
}

// Animations
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

// Responsive Design
@media (max-width: 768px) {
    .parcours-item {
        padding: var(--spacing-lg);
        gap: var(--spacing-md);

        &:hover {
            transform: translateY(-1px);
        }
    }

    .sport-icon {
        margin-bottom: var(--spacing-xs);
        width: 55px;
        height: 55px;
        font-size: 1.6rem;
    }

    .intro-quote {
        padding: var(--spacing-md);
        font-size: clamp(1.1rem, 4vw, 1.3rem);

        &::before {
            width: 50px;
            height: 20px;
            right: 15px;
            top: -5px;
        }
    }

    .conclusion-quote {
        padding: var(--spacing-lg);
        font-size: clamp(1rem, 3vw, 1.1rem);

        &::before {
            font-size: 1.5rem;
            top: -10px;
        }

        &::after {
            width: 60px;
            height: 3px;
        }
    }
}

@media (max-width: 480px) {
    .parcours-item {
        padding: var(--spacing-md);
        gap: var(--spacing-sm);
    }

    .sport-icon {
        width: 50px;
        height: 50px;
        font-size: 1.4rem;
    }

    .content {
        h3 {
            font-size: clamp(1.1rem, 4vw, 1.3rem);
        }

        p {
            font-size: clamp(0.9rem, 3vw, 1rem);
            padding-top: var(--spacing-sm);
        }
    }
}
</style>
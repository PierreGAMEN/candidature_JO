<script setup lang="ts">
import SectionPart from "../sectionPart.vue"

//script a placer ici 
</script>

<template>
    <SectionPart title="Construire ensemble un projet qui fait sens, au cœur des Alpes" altImage="Logo JO">
        <template #default>
            <div class="adventure-content">
                <p class="intro-text">
                    Ces Jeux
                    ne sont pas un simple événement : ils représentent une <strong>opportunité unique</strong> de
                    contribuer à l’avenir
                    de mon territoire, <em>les Alpes</em>, que je connais, aime et respecte profondément.
                </p>

                <div class="motivation-section">
                    <h3>Pourquoi rejoindre cette aventure olympique ?</h3>

                    <div class="reasons-list">
                        <div class="reason-item">
                            <span class="icon">🏔️</span>
                            <div class="content">
                                <h4>Un engagement local, naturel et sincère</h4>
                                <p>
                                    Né et élevé dans les Alpes, j’y ai forgé ma persévérance à travers les sports de
                                    montagne : ski de fond, ski alpin, alpinisme, escalade, trail… Ce territoire m’a
                                    construit. C’est pourquoi je souhaite m’engager pour lui, en contribuant à une
                                    organisation respectueuse de son environnement et résolument tournée vers l’avenir.
                                </p>

                            </div>
                        </div>

                        <div class="reason-item">
                            <span class="icon">🤝</span>
                            <div class="content">
                                <h4>Un savoir-faire issu du terrain et du collectif</h4>
                                <p>Huit années chez Decathlon et mon expérience en tant que développeur web m’ont formé
                                    à la gestion d’équipe, la rigueur
                                    opérationnelle, et la coordination de projets. J’apporte aujourd’hui ces
                                    compétence humaine et technique, avec une
                                    conviction forte : la réussite naît de l’intelligence collective.</p>
                            </div>
                        </div>

                        <div class="reason-item">
                            <span class="icon">🌱</span>
                            <div class="content">
                                <h4>Une vision partagée avec l’organisation 2030</h4>
                                <p>Sobriété, inclusion, durabilité : ce sont des principes que je partage et que
                                    j’applique au quotidien. Mon objectif est de contribuer à des solutions concrètes,
                                    utiles et responsables, pour maximiser l’héritage de ces Jeux.</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="engagement">
                    <blockquote class="blockquote-accent">
                        Mon engagement : mettre toute mon énergie au service de Jeux exemplaires,
                        ancrés dans leur territoire et tournés vers l'avenir.
                    </blockquote>
                </div>
            </div>
        </template>
    </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.adventure-content {
    // Variables locales pour la cohérence
    --spacing-sm: 0.75rem;
    --spacing-md: 1.5rem;
    --spacing-lg: 2.5rem;
    --border-radius: 16px;
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

    .intro-text {
        font-size: clamp(1.1rem, 2.5vw, 1.25rem);
        line-height: 1.8;
        color: #2d3748;
        margin-bottom: var(--spacing-lg);
        font-weight: 400;
        letter-spacing: 0.01em;
        text-align: center;

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
        margin-bottom: var(--spacing-lg);

        h3 {
            color: $primary-color;
            font-size: clamp(1.25rem, 3vw, 1.5rem);
            font-weight: 700;
            margin-bottom: var(--spacing-md);
            text-align: center;
            position: relative;
            padding-bottom: 0.5rem;

            &::after {
                content: '';
                position: absolute;
                bottom: 0;
                left: 50%;
                transform: translateX(-50%);
                width: 60px;
                height: 3px;
                background: linear-gradient(90deg, $primary-color, lighten($primary-color, 30%));
                border-radius: 2px;
            }
        }

        .reasons-list {
            display: grid;
            gap: var(--spacing-md);

            .reason-item {
                display: flex;
                align-items: flex-start;
                gap: var(--spacing-md);
                padding: var(--spacing-md);
                background: linear-gradient(135deg, #ffffff 0%, #f8fafc 100%);
                border-radius: var(--border-radius);
                border: 1px solid rgba($primary-color, 0.08);
                box-shadow: 0 4px 6px rgba(0, 0, 0, 0.02), 0 1px 3px rgba(0, 0, 0, 0.06);
                position: relative;
                overflow: hidden;
                transition: var(--transition);

                &::before {
                    content: '';
                    position: absolute;
                    top: 0;
                    left: 0;
                    width: 4px;
                    height: 100%;
                    background: linear-gradient(180deg, $primary-color, lighten($primary-color, 20%));
                }

                &:hover {
                    transform: translateY(-2px) scale(1.01);
                    box-shadow: 0 12px 25px rgba($primary-color, 0.1), 0 4px 10px rgba(0, 0, 0, 0.08);
                    border-color: rgba($primary-color, 0.15);

                    .icon {
                        transform: scale(1.1);
                    }
                }

                .icon {
                    font-size: 2.25rem;
                    flex-shrink: 0;
                    transition: var(--transition);
                    filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.1));
                }

                .content {
                    flex: 1;

                    h4 {
                        color: $primary-color;
                        font-size: clamp(1.1rem, 2.5vw, 1.25rem);
                        font-weight: 600;
                        margin: 0 0 var(--spacing-sm) 0;
                        letter-spacing: -0.01em;
                        line-height: 1.3;
                    }

                    p {
                        color: #4a5568;
                        font-size: clamp(0.95rem, 2vw, 1.05rem);
                        line-height: 1.6;
                        margin: 0;
                        font-weight: 400;
                    }
                }
            }
        }
    }

    .engagement {
        margin-top: var(--spacing-lg);
    }

    // Responsive optimisé
    @media (max-width: 768px) {
        .motivation-section {
            .reasons-list .reason-item {
                padding: var(--spacing-md);
                gap: var(--spacing-md);

                .icon {
                    font-size: 1.75rem;
                }
            }
        }
    }

    @media (max-width: 480px) {
        .motivation-section .reasons-list .reason-item {
            flex-direction: column;
            text-align: center;
            gap: var(--spacing-sm);

            .icon {
                align-self: center;
                font-size: 2rem;
            }
        }
    }
}
</style>

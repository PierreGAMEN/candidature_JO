<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>

<template>
    <SectionPart title="Qui suis-je professionnellement ?">
        <template #default>
            <div class="professionnel-content">
                <div class="intro-section">
                    <p class="intro-text">
                        Mon parcours professionnel combine <strong>management d'équipes</strong> et
                        <strong>développement numérique</strong> : une approche qui allie vision d'ensemble
                        et mise en œuvre technique.
                    </p>
                </div>

                <div class="experience-section">
                    <div class="experience-item">
                        <div class="exp-icon">🏢</div>
                        <div class="exp-content">
                            <h3>8 ans chez Decathlon</h3>
                            <div class="exp-subtitle">Manager & Pilote opérationnel</div>
                            <p>
                                Responsable d'équipes de 15 à 20 personnes, j'ai développé des compétences en
                                <strong>coordination de projets</strong> et <strong>amélioration continue</strong>.
                                Pilotage de transformations opérationnelles dans un environnement exigeant.
                            </p>
                            <ul class="skills-list">
                                <li>Management d'équipes pluridisciplinaires</li>
                                <li>Pilotage de projets transversaux</li>
                                <li>Formation et développement des talents</li>
                            </ul>
                        </div>
                    </div>

                    <div class="experience-item">
                        <div class="exp-icon">💻</div>
                        <div class="exp-content">
                            <h3>Développeur Web</h3>
                            <div class="exp-subtitle">Solutions numériques modernes</div>
                            <p>
                                Je conçois et développe des <strong>solutions web</strong>
                                modernes en privilégiant l'<em>expérience utilisateur</em> et
                                la <strong>performance</strong>.
                            </p>
                            <ul class="skills-list">
                                <li>Développement Frontend (Vue.js, React, TypeScript)</li>
                                <li>Conception UX/UI centrée utilisateur</li>
                                <li>Architecture et optimisation web</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="competences-section">
                    <h3>Compétences transversales</h3>
                    <div class="competences-grid">
                        <div class="competence-card">
                            <div class="comp-icon">🎯</div>
                            <h4>Leadership</h4>
                            <p>Animation d'équipes et vision stratégique</p>
                        </div>

                        <div class="competence-card">
                            <div class="comp-icon">🔧</div>
                            <h4>Résolution de problèmes</h4>
                            <p>Analyse et amélioration des processus</p>
                        </div>

                        <div class="competence-card">
                            <div class="comp-icon">🤝</div>
                            <h4>Communication</h4>
                            <p>Collaboration et partage des savoirs</p>
                        </div>

                        <div class="competence-card">
                            <div class="comp-icon">⚡</div>
                            <h4>Adaptabilité</h4>
                            <p>Agilité et accompagnement du changement</p>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </SectionPart>
</template>

<style scoped lang="scss">
@use '@/styles/variables' as *;

.professionnel-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
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
    max-width: 800px;
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

.experience-section {
    margin: var(--spacing-xl) 0;
    display: flex;
    flex-direction: column;
    gap: var(--spacing-xl);
}

.experience-item {
    display: flex;
    gap: var(--spacing-lg);
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    padding: var(--spacing-xl);
    border: 1px solid rgba(0, 0, 0, 0.08);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }

    .exp-icon {
        width: 80px;
        height: 80px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 2.5rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        flex-shrink: 0;
    }

    .exp-content {
        flex: 1;

        h3 {
            font-size: clamp(1.3rem, 2.5vw, 1.6rem);
            font-weight: 600;
            color: var(--text-primary);
            margin: 0 0 var(--spacing-xs) 0;
            line-height: 1.3;
        }

        .exp-subtitle {
            font-size: clamp(1rem, 2vw, 1.1rem);
            color: $primary-color;
            font-weight: 500;
            margin-bottom: var(--spacing-md);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            font-size: 0.9rem;
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

            em {
                color: $primary-color;
                font-style: normal;
                font-weight: 500;
            }
        }
    }
}

.skills-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: var(--spacing-sm);

    li {
        font-size: clamp(0.9rem, 1.6vw, 1rem);
        color: var(--text-secondary);
        padding: var(--spacing-xs) var(--spacing-sm);
        background: rgba($primary-color, 0.05);
        border-radius: var(--border-radius);
        border-left: 3px solid $primary-color;
        position: relative;

        &::before {
            content: '✓';
            color: $primary-color;
            font-weight: bold;
            margin-right: var(--spacing-xs);
        }
    }
}

.competences-section {
    margin: var(--spacing-xl) 0;
    text-align: center;

    h3 {
        font-size: clamp(1.4rem, 2.8vw, 1.8rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-xl) 0;
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

.competences-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: var(--spacing-lg);
}

.competence-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    padding: var(--spacing-lg);
    border: 1px solid rgba(0, 0, 0, 0.08);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
    text-align: center;

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }

    .comp-icon {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.5rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        margin: 0 auto var(--spacing-md);
    }

    h4 {
        font-size: clamp(1.1rem, 2vw, 1.2rem);
        font-weight: 500;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-sm) 0;
    }

    p {
        font-size: clamp(0.9rem, 1.8vw, 1rem);
        line-height: 1.6;
        color: var(--text-secondary);
        margin: 0;
    }
}

.value-proposition {
    margin-top: var(--spacing-xl);
    text-align: center;
}

.value-quote {
    font-size: clamp(1.1rem, 2.5vw, 1.3rem);
    line-height: 1.7;
    color: var(--text-primary);
    font-weight: 300;
    font-style: italic;
    margin: 0;
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.08), rgba($primary-color, 0.03));
    border-radius: var(--border-radius-lg);
    border: 2px solid rgba($primary-color, 0.15);
    max-width: 800px;
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

.intro-section {
    animation: fadeInUp 0.6s ease-out;
}

.experience-item {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    &:nth-child(1) {
        animation-delay: 0.2s;
    }

    &:nth-child(2) {
        animation-delay: 0.4s;
    }
}

.competences-section {
    animation: fadeInUp 0.6s ease-out 0.6s;
    animation-fill-mode: both;
}

.competence-card {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    &:nth-child(1) {
        animation-delay: 0.8s;
    }

    &:nth-child(2) {
        animation-delay: 1s;
    }

    &:nth-child(3) {
        animation-delay: 1.2s;
    }

    &:nth-child(4) {
        animation-delay: 1.4s;
    }
}

.value-proposition {
    animation: fadeInUp 0.6s ease-out 1.6s;
    animation-fill-mode: both;
}

// Responsive Design
@media (max-width: 768px) {
    .experience-item {
        flex-direction: column;
        text-align: center;
        gap: var(--spacing-md);

        .exp-icon {
            width: 60px;
            height: 60px;
            font-size: 2rem;
            margin: 0 auto;
        }
    }

    .skills-list {
        grid-template-columns: 1fr;
    }

    .competences-grid {
        grid-template-columns: 1fr;
        gap: var(--spacing-md);
    }

    .value-quote {
        padding: var(--spacing-lg);
    }
}

@media (max-width: 480px) {
    .experience-item {
        padding: var(--spacing-lg);
    }

    .competence-card {
        padding: var(--spacing-md);
    }
}
</style>

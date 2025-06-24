<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>

<template>
    <SectionPart title="Ce que je recherche et contact">
        <template #default>
            <div class="recherche-content">
                <div class="recherche-section">
                    <div class="recherche-intro">
                        <p class="intro-text">
                            Mon objectif : mettre mes compétences au service d'un projet <em>ambitieux</em>
                            qui peut marquer positivement le sport et le territoire.
                        </p>
                    </div>

                    <div class="objectifs-grid">
                        <div class="objectif-card">
                            <div class="obj-icon">🎯</div>
                            <h4>Mission recherchée</h4>
                            <ul class="objectif-list">
                                <li>Coordination de projets olympiques</li>
                                <li>Management d'équipes opérationnelles</li>
                                <li>Développement de solutions digitales</li>
                                <li>Interface avec les partenaires locaux</li>
                            </ul>
                        </div>

                        <div class="objectif-card">
                            <div class="obj-icon">🌟</div>
                            <h4>Ambitions</h4>
                            <ul class="objectif-list">
                                <li>Contribuer à des Jeux durables et réussis</li>
                                <li>Participer à la valorisation du territoire alpin</li>
                                <li>Participer à l'innovation dans l'expérience olympique</li>
                                <li>Contribuer à un héritage positif</li>
                            </ul>
                        </div>

                        <div class="objectif-card">
                            <div class="obj-icon">🤝</div>
                            <h4>Environnement recherché</h4>
                            <ul class="objectif-list">
                                <li>Équipe collaborative et ambitieuse</li>
                                <li>Projets à fort impact</li>
                                <li>Innovation et excellence opérationnelle</li>
                                <li>Respect des valeurs olympiques</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="contact-section">
                    <div class="contact-intro">
                        <h3>Prenons contact</h3>
                        <p class="contact-text">
                            Prêt à échanger sur les opportunités de collaboration pour faire des
                            <strong>Jeux Olympiques d'hiver 2030</strong> un événement inoubliable.
                        </p>
                    </div>

                    <div class="contact-content">
                        <div class="contact-info">
                            <div class="contact-card">
                                <div class="contact-icon">📧</div>
                                <div class="contact-details">
                                    <h4>Email</h4>
                                    <a href="mailto:pierre.gamen@email.com" class="contact-link">
                                        pierre.gamen@email.com
                                    </a>
                                </div>
                            </div>

                            <div class="contact-card">
                                <div class="contact-icon">📱</div>
                                <div class="contact-details">
                                    <h4>Téléphone</h4>
                                    <a href="tel:0673607777" class="contact-link">
                                        +33 6 73 60 77 77
                                    </a>
                                </div>
                            </div>

                            <div class="contact-card">
                                <div class="contact-icon">💼</div>
                                <div class="contact-details">
                                    <h4>LinkedIn</h4>
                                    <a href="https://www.linkedin.com/in/pierre-gamen" target="_blank" class="contact-link">
                                        Pierre GAMEN
                                    </a>
                                </div>
                            </div>
                        </div>

                        <div class="disponibilite">
                            <div class="dispo-card">
                                <div class="dispo-icon">📅</div>
                                <div class="dispo-content">
                                    <h4>Disponibilité</h4>
                                    <p>
                                        <strong>Immédiate</strong> pour un entretien ou une présentation détaillée de
                                        mon profil.
                                        Flexible sur les modalités de collaboration.
                                    </p>
                                    <div class="dispo-details">
                                        <span class="dispo-item">💬 Entretien en personne ou visio</span>
                                        <span class="dispo-item">🤝 Rencontre avec l'équipe</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="cta-final">
                    <div class="cta-content">
                        <h3>Construisons ensemble les Jeux de demain</h3>
                        <p class="cta-text">
                            Les <strong>Jeux Olympiques d'hiver 2030</strong> représentent une belle opportunité
                            de créer un événement réussi. Mon expérience, ma motivation et mon ancrage territorial
                            peuvent contribuer à cette ambition.
                        </p>
                        <div class="cta-actions">
                            <a href="mailto:pierre.gamen@email.com" class="cta-button primary">
                                <span class="button-icon">📧</span>
                                Me contacter
                            </a>
                            <a href="tel:+33123456789" class="cta-button secondary">
                                <span class="button-icon">📱</span>
                                Appeler
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </SectionPart>
</template>

<style scoped lang="scss">
@use '@/styles/variables' as *;

.recherche-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
}

.recherche-section {
    margin-bottom: var(--spacing-xl);
}

.recherche-intro {
    text-align: center;
    margin-bottom: var(--spacing-xl);

    h3 {
        font-size: clamp(1.5rem, 3vw, 2rem);
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
}

.objectifs-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-lg);
}

.objectif-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    padding: var(--spacing-xl);
    border: 1px solid rgba(0, 0, 0, 0.08);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
    text-align: center;

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }

    .obj-icon {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.8rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        margin: 0 auto var(--spacing-lg);
    }

    h4 {
        font-size: clamp(1.2rem, 2.2vw, 1.4rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-md) 0;
    }
}

.objectif-list {
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: left;

    li {
        font-size: clamp(0.95rem, 1.8vw, 1.05rem);
        color: var(--text-secondary);
        padding: var(--spacing-xs) 0;
        position: relative;
        padding-left: 1.5rem;

        &::before {
            content: '✓';
            color: $primary-color;
            font-weight: bold;
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

.contact-section {
    margin: var(--spacing-xl) 0;
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.05), rgba(255, 255, 255, 0.98));
    border-radius: var(--border-radius-lg);
    border: 1px solid rgba($primary-color, 0.15);
}

.contact-intro {
    text-align: center;
    margin-bottom: var(--spacing-xl);

    h3 {
        font-size: clamp(1.5rem, 3vw, 2rem);
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

    .contact-text {
        font-size: clamp(1.1rem, 2.2vw, 1.25rem);
        line-height: 1.6;
        color: var(--text-primary);
        margin: 0;
        max-width: 600px;
        margin: 0 auto;

        strong {
            font-weight: 600;
            color: $primary-color;
        }
    }
}

.contact-content {
    display: grid;
    grid-template-columns: 1fr;
    gap: var(--spacing-xl);
    align-items: start;
}

.contact-info {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: var(--spacing-lg);
}

.contact-card {
    display: flex;
    align-items: center;
    gap: var(--spacing-md);
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius);
    padding: var(--spacing-lg);
    border: 1px solid rgba(0, 0, 0, 0.08);
    transition: all 0.3s ease;

    &:hover {
        transform: translateY(-1px);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    .contact-icon {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.5rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        flex-shrink: 0;
    }

    .contact-details {
        flex: 1;

        h4 {
            font-size: 1.1rem;
            font-weight: 500;
            color: var(--text-primary);
            margin: 0 0 var(--spacing-xs) 0;
        }

        .contact-link {
            color: $primary-color;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;

            &:hover {
                color: darken($primary-color, 10%);
                text-decoration: underline;
            }
        }

        .contact-note {
            font-size: 0.85rem;
            color: var(--text-secondary);
            margin: var(--spacing-xs) 0 0 0;
        }
    }
}

.disponibilite {
    width: 100%;
}

.dispo-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    padding: var(--spacing-xl);
    border: 2px solid rgba($primary-color, 0.15);
    text-align: center;

    .dispo-icon {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.8rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.15), rgba($primary-color, 0.08));
        border: 2px solid rgba($primary-color, 0.2);
        margin: 0 auto var(--spacing-lg);
    }

    h4 {
        font-size: clamp(1.2rem, 2.2vw, 1.4rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-md) 0;
    }

    p {
        font-size: clamp(1rem, 1.8vw, 1.1rem);
        line-height: 1.6;
        color: var(--text-secondary);
        margin: 0 0 var(--spacing-lg) 0;

        strong {
            color: $primary-color;
            font-weight: 600;
        }
    }

    .dispo-details {
        display: flex;
        flex-wrap: wrap;
        gap: var(--spacing-sm);
        justify-content: center;

        .dispo-item {
            font-size: 0.9rem;
            color: var(--text-secondary);
            background: rgba($primary-color, 0.05);
            padding: var(--spacing-xs) var(--spacing-sm);
            border-radius: var(--border-radius);
            border: 1px solid rgba($primary-color, 0.1);
        }
    }
}

.cta-final {
    margin-top: var(--spacing-xl);
    text-align: center;
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.08), rgba($primary-color, 0.03));
    border-radius: var(--border-radius-lg);
    border: 2px solid rgba($primary-color, 0.15);
}

.cta-content {
    h3 {
        font-size: clamp(1.5rem, 3vw, 2rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-lg) 0;
    }

    .cta-text {
        font-size: clamp(1.1rem, 2.2vw, 1.25rem);
        line-height: 1.6;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-xl) 0;
        max-width: 700px;
        margin-left: auto;
        margin-right: auto;

        strong {
            font-weight: 600;
            color: $primary-color;
        }
    }
}

.cta-actions {
    display: flex;
    gap: var(--spacing-lg);
    justify-content: center;
    flex-wrap: wrap;
}

.cta-button {
    display: inline-flex;
    align-items: center;
    gap: var(--spacing-sm);
    padding: var(--spacing-md) var(--spacing-xl);
    border-radius: var(--border-radius);
    text-decoration: none;
    font-weight: 500;
    font-size: 1.1rem;
    transition: all 0.3s ease;
    border: 2px solid;

    .button-icon {
        font-size: 1.2rem;
    }

    &.primary {
        background: $primary-color;
        color: white;
        border-color: $primary-color;

        &:hover {
            background: darken($primary-color, 10%);
            border-color: darken($primary-color, 10%);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba($primary-color, 0.3);
        }
    }

    &.secondary {
        background: transparent;
        color: $primary-color;
        border-color: $primary-color;

        &:hover {
            background: $primary-color;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba($primary-color, 0.3);
        }
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

.recherche-intro {
    animation: fadeInUp 0.6s ease-out;
}

.objectif-card {
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
}

.contact-section {
    animation: fadeInUp 0.6s ease-out 0.8s;
    animation-fill-mode: both;
}

.cta-final {
    animation: fadeInUp 0.6s ease-out 1s;
    animation-fill-mode: both;
}

// Responsive Design
@media (max-width: 768px) {
    .objectifs-grid {
        grid-template-columns: 1fr;
        gap: var(--spacing-md);
    }

    .contact-info {
        grid-template-columns: 1fr;
    }

    .dispo-details {
        .dispo-item {
            flex: 1;
            text-align: center;
        }
    }

    .cta-actions {
        flex-direction: column;
        align-items: center;

        .cta-button {
            width: 100%;
            max-width: 300px;
            justify-content: center;
        }
    }
}

@media (max-width: 480px) {

    .contact-section,
    .cta-final {
        padding: var(--spacing-lg);
    }

    .objectif-card,
    .dispo-card {
        padding: var(--spacing-lg);
    }

    .contact-card {
        flex-direction: column;
        text-align: center;
        gap: var(--spacing-sm);
    }
}
</style>

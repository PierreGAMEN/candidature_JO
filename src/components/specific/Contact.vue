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
    <SectionPart title="Ce que je recherche">
        <template #default>
            <div class="contact-content">
                <div class="missions-section">
                    <h3>Missions recherchées</h3>
                    <div class="missions-grid">
                        <div class="mission-item">
                            <span class="mission-icon">🎯</span>
                            <span>Coordination de projets olympiques</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">👥</span>
                            <span>Management d'équipes opérationnelles</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">💻</span>
                            <span>Développement de solutions digitales</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">🏔️</span>
                            <span>Interface avec les partenaires locaux</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">📋</span>
                            <span>Pilotage de la logistique événementielle</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">🔧</span>
                            <span>Amélioration continue des processus</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">🌐</span>
                            <span>Développement d'outils numériques JO</span>
                        </div>
                        <div class="mission-item">
                            <span class="mission-icon">🤝</span>
                            <span>Liaison avec les collectivités alpines</span>
                        </div>
                    </div>
                </div>

                <div class="contact-section">
                    <h3>Contact</h3>
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
    max-width: 800px;
}

.missions-section,
.contact-section {
    text-align: center;

    h3 {
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

.missions-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: var(--spacing-md);
    margin-top: var(--spacing-lg);
}

.mission-item {
    display: flex;
    align-items: center;
    gap: var(--spacing-sm);
    padding: var(--spacing-md);
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius);
    border: 1px solid rgba(0, 0, 0, 0.08);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
    text-align: left;

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        border-color: rgba($primary-color, 0.2);
    }

    .mission-icon {
        font-size: 1.5rem;
        flex-shrink: 0;
    }

    span:last-child {
        font-size: clamp(0.95rem, 1.8vw, 1.05rem);
        font-weight: 500;
        color: var(--text-primary);
        line-height: 1.4;
    }
}

.contact-buttons {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: var(--spacing-md);
    width: 100%;
    margin-top: var(--spacing-lg);
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

.missions-section {
    animation: fadeInUp 0.6s ease-out;
}

.contact-section {
    animation: fadeInUp 0.6s ease-out 0.2s;
    animation-fill-mode: both;
}

.mission-item {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

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

    &:nth-child(7) {
        animation-delay: 0.7s;
    }

    &:nth-child(8) {
        animation-delay: 0.8s;
    }
}

// Responsive Design
@media (max-width: 768px) {
    .missions-grid {
        grid-template-columns: 1fr;
        gap: var(--spacing-sm);
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
}
</style>

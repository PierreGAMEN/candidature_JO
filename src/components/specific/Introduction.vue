<script setup lang="ts">
import SectionPart from '../sectionPart.vue';
</script>

<template>
    <SectionPart title="Présentation">
        <template #default>
            <div class="introduction-content">
                <div class="intro-hero">
                    <div class="hero-main">
                        <div class="profile-content">
                            <div class="profile-image-section">
                                <img src="/photoPg.png" alt="Pierre GAMEN" class="main-photo" />
                                <div class="olympic-badge">
                                    <div class="olympic-rings-mini"></div>
                                </div>
                            </div>
                            <div class="profile-info">
                                <h2 class="profile-name">Pierre GAMEN</h2>
                                <p class="profile-subtitle">Manager • Développeur • Sportif</p>
                            </div>
                        </div>
                    </div>

                    <div class="elevator-pitch">
                        <blockquote class="pitch-quote">
                            « <strong>Manager</strong>, <strong>développeur web</strong>
                            et <em>sportif orienté montagne</em>.
                            Je souhaite mettre mon expérience au service des
                            <strong>JO 2030</strong> dans les Alpes françaises. »
                        </blockquote>
                    </div>

                    <div class="key-points">
                        <div class="point">
                            <div class="point-icon">🏔️</div>
                            <h3>Ancrage alpin</h3>
                            <p>Né dans les Alpes, pratique de la montagne depuis l'enfance</p>
                        </div>

                        <div class="point">
                            <div class="point-icon">💼</div>
                            <h3>Double expertise</h3>
                            <p>Management d'équipes + développement de solutions numériques</p>
                        </div>

                        <div class="point">
                            <div class="point-icon">🏆</div>
                            <h3>Légitimité sportive</h3>
                            <p>Pratique de plusieurs sports présents aux JO d'hiver</p>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </SectionPart>
</template>

<style scoped lang="scss">
@use '@/styles/variables' as *;

.introduction-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
}

.intro-hero {
    text-align: center;
    padding: var(--spacing-xl) 0;
}

.hero-main {
    margin-bottom: var(--spacing-xl);
}

.profile-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: var(--spacing-lg);
    max-width: 600px;
    margin: 0 auto;
}

.profile-image-section {
    position: relative;
    display: inline-block;
}

.main-photo {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid rgba($primary-color, 0.2);
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease;

    &:hover {
        transform: scale(1.05);
        box-shadow: 0 12px 40px rgba(0, 0, 0, 0.2);
    }
}

.olympic-badge {
    position: absolute;
    bottom: 10px;
    right: 10px;
    width: 50px;
    height: 50px;
    background: rgba(255, 255, 255, 0.95);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    border: 2px solid rgba($primary-color, 0.3);
}

.olympic-rings-mini {
    width: 30px;
    height: 18px;
    background:
        radial-gradient(circle at 4px 9px, transparent 2px, rgba(0, 133, 195, 0.9) 2px, rgba(0, 133, 195, 0.9) 3px, transparent 3px),
        radial-gradient(circle at 10px 9px, transparent 2px, rgba(51, 51, 51, 0.9) 2px, rgba(51, 51, 51, 0.9) 3px, transparent 3px),
        radial-gradient(circle at 16px 9px, transparent 2px, rgba(238, 51, 78, 0.9) 2px, rgba(238, 51, 78, 0.9) 3px, transparent 3px),
        radial-gradient(circle at 22px 9px, transparent 2px, rgba(255, 209, 0, 0.9) 2px, rgba(255, 209, 0, 0.9) 3px, transparent 3px),
        radial-gradient(circle at 28px 9px, transparent 2px, rgba(0, 166, 81, 0.9) 2px, rgba(0, 166, 81, 0.9) 3px, transparent 3px);
}

.profile-info {
    text-align: center;

    .profile-name {
        font-size: clamp(1.8rem, 4vw, 2.2rem);
        font-weight: 700;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-sm) 0;
        line-height: 1.2;
    }

    .profile-subtitle {
        font-size: clamp(1rem, 2.5vw, 1.2rem);
        color: $primary-color;
        font-weight: 500;
        margin: 0;
        text-transform: uppercase;
        letter-spacing: 1px;
    }
}

.profile-image {
    position: relative;
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
    border: 3px solid rgba($primary-color, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3rem;

    &::before {
        content: '👨‍💼';
        display: block;
    }

    .olympic-rings {
        position: absolute;
        top: -10px;
        right: -10px;
        width: 40px;
        height: 25px;
        background:
            radial-gradient(circle at 6px 12px, transparent 3px, rgba(0, 133, 195, 0.8) 3px, rgba(0, 133, 195, 0.8) 5px, transparent 5px),
            radial-gradient(circle at 14px 12px, transparent 3px, rgba(51, 51, 51, 0.8) 3px, rgba(51, 51, 51, 0.8) 5px, transparent 5px),
            radial-gradient(circle at 22px 12px, transparent 3px, rgba(238, 51, 78, 0.8) 3px, rgba(238, 51, 78, 0.8) 5px, transparent 5px),
            radial-gradient(circle at 30px 12px, transparent 3px, rgba(255, 209, 0, 0.8) 3px, rgba(255, 209, 0, 0.8) 5px, transparent 5px),
            radial-gradient(circle at 38px 12px, transparent 3px, rgba(0, 166, 81, 0.8) 3px, rgba(0, 166, 81, 0.8) 5px, transparent 5px);
        border-radius: 50%;
        background-color: white;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
}

.profile-text {
    h2 {
        font-size: clamp(1.8rem, 4vw, 2.5rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 var(--spacing-sm) 0;
        line-height: 1.2;
    }

    .subtitle {
        font-size: clamp(1.2rem, 2.5vw, 1.5rem);
        color: $primary-color;
        font-weight: 500;
        margin: 0;
        text-transform: uppercase;
        letter-spacing: 1px;
    }
}

.elevator-pitch {
    margin: var(--spacing-xl) 0;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
}

.pitch-quote {
    font-size: clamp(1.2rem, 2.8vw, 1.6rem);
    line-height: 1.6;
    color: var(--text-primary);
    font-weight: 300;
    font-style: italic;
    margin: 0;
    padding: var(--spacing-xl);
    background: linear-gradient(135deg, rgba($primary-color, 0.08), rgba(255, 255, 255, 0.95));
    border-radius: var(--border-radius-lg);
    border-left: 4px solid $primary-color;
    box-shadow: var(--shadow-md);
    position: relative;

    strong {
        font-weight: 600;
        color: var(--text-primary);
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

.key-points {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: var(--spacing-lg);
    margin-top: var(--spacing-xl);
}

.point {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: var(--spacing-lg);
    background: rgba(255, 255, 255, 0.95);
    border-radius: var(--border-radius-lg);
    border: 1px solid rgba(0, 0, 0, 0.08);
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }

    .point-icon {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.8rem;
        background: linear-gradient(135deg, rgba($primary-color, 0.1), rgba($primary-color, 0.05));
        border: 2px solid rgba($primary-color, 0.15);
        margin-bottom: var(--spacing-md);
    }

    h3 {
        font-size: clamp(1.1rem, 2.2vw, 1.3rem);
        font-weight: 500;
        margin: 0 0 var(--spacing-sm) 0;
        color: var(--text-primary);
        line-height: 1.3;
    }

    p {
        font-size: clamp(0.95rem, 1.8vw, 1.05rem);
        line-height: 1.6;
        color: var(--text-secondary);
        margin: 0;
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

.profile-content {
    animation: fadeInUp 0.3s ease-out;
}

.elevator-pitch {
    animation: fadeInUp 0.3s ease-out 0.1s;
    animation-fill-mode: both;
}

.point {
    animation: fadeInUp 0.3s ease-out;
    animation-fill-mode: both;

    &:nth-child(1) {
        animation-delay: 0.2s;
    }

    &:nth-child(2) {
        animation-delay: 0.3s;
    }

    &:nth-child(3) {
        animation-delay: 0.4s;
    }
}

// Responsive Design
@media (max-width: 768px) {
    .main-photo {
        width: 160px;
        height: 160px;
    }

    .olympic-badge {
        width: 40px;
        height: 40px;
        bottom: 8px;
        right: 8px;
    }

    .olympic-rings-mini {
        width: 24px;
        height: 14px;
        background:
            radial-gradient(circle at 3px 7px, transparent 1.5px, rgba(0, 133, 195, 0.9) 1.5px, rgba(0, 133, 195, 0.9) 2.5px, transparent 2.5px),
            radial-gradient(circle at 8px 7px, transparent 1.5px, rgba(51, 51, 51, 0.9) 1.5px, rgba(51, 51, 51, 0.9) 2.5px, transparent 2.5px),
            radial-gradient(circle at 13px 7px, transparent 1.5px, rgba(238, 51, 78, 0.9) 1.5px, rgba(238, 51, 78, 0.9) 2.5px, transparent 2.5px),
            radial-gradient(circle at 18px 7px, transparent 1.5px, rgba(255, 209, 0, 0.9) 1.5px, rgba(255, 209, 0, 0.9) 2.5px, transparent 2.5px),
            radial-gradient(circle at 23px 7px, transparent 1.5px, rgba(0, 166, 81, 0.9) 1.5px, rgba(0, 166, 81, 0.9) 2.5px, transparent 2.5px);
    }

    .key-points {
        grid-template-columns: 1fr;
        gap: var(--spacing-md);
    }

    .pitch-quote {
        padding: var(--spacing-lg);
        font-size: clamp(1.1rem, 4vw, 1.3rem);
    }

    .profile-image {
        width: 100px;
        height: 100px;
        font-size: 2.5rem;

        .olympic-rings {
            width: 35px;
            height: 20px;
            top: -8px;
            right: -8px;
        }
    }
}

@media (max-width: 480px) {
    .main-photo {
        width: 140px;
        height: 140px;
        border-width: 3px;
    }

    .olympic-badge {
        width: 35px;
        height: 35px;
        bottom: 5px;
        right: 5px;
    }

    .olympic-rings-mini {
        width: 20px;
        height: 12px;
        background:
            radial-gradient(circle at 2.5px 6px, transparent 1px, rgba(0, 133, 195, 0.9) 1px, rgba(0, 133, 195, 0.9) 2px, transparent 2px),
            radial-gradient(circle at 6.5px 6px, transparent 1px, rgba(51, 51, 51, 0.9) 1px, rgba(51, 51, 51, 0.9) 2px, transparent 2px),
            radial-gradient(circle at 10.5px 6px, transparent 1px, rgba(238, 51, 78, 0.9) 1px, rgba(238, 51, 78, 0.9) 2px, transparent 2px),
            radial-gradient(circle at 14.5px 6px, transparent 1px, rgba(255, 209, 0, 0.9) 1px, rgba(255, 209, 0, 0.9) 2px, transparent 2px),
            radial-gradient(circle at 18.5px 6px, transparent 1px, rgba(0, 166, 81, 0.9) 1px, rgba(0, 166, 81, 0.9) 2px, transparent 2px);
    }

    .profile-content {
        gap: var(--spacing-md);
    }

    .point {
        padding: var(--spacing-md);
    }

    .profile-image {
        width: 80px;
        height: 80px;
        font-size: 2rem;
    }
}
</style>

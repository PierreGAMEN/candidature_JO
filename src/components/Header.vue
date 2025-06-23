<template>
    <header class="hero-banner">
        <div class="hero-background"></div>
        <div class="hero-container">
            <div class="hero-content">
                <!-- Logos desktop (cachés en mobile) -->
                <div class="logo-left">
                    <img src="/logoJO.png" alt="Logo JO" class="logo-desktop" />
                </div>

                <!-- Divider gauche (caché en mobile) -->
                <div class="divider divider-left"></div>

                <!-- Contenu central -->
                <div class="hero-text">
                    <h1 class="hero-title">PIERRE GAMEN</h1>
                    <p class="hero-subtitle">Futur acteur des Jeux Olympiques et Paralympiques d'hiver</p>
                </div>

                <!-- Divider droit (caché en mobile) -->
                <div class="divider divider-right"></div>

                <!-- Logo droit desktop (caché en mobile) -->
                <div class="logo-right">
                    <img src="/logo-paralympique.png" alt="Logo Paralympique" class="logo-desktop" />
                </div>

                <!-- Logos mobile (cachés en desktop) -->
                <div class="logos-mobile">
                    <img src="/logoJO.png" alt="Logo JO" class="logo-mobile" />
                    <img src="/logo-paralympique.png" alt="Logo Paralympique" class="logo-mobile" />
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '@/styles/variables' as *;

.hero-banner {
    position: relative;
    min-height: clamp(280px, 45vh, 400px);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    width: 100%;
    box-sizing: border-box;
}

.hero-background {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background:
        linear-gradient(135deg,
            rgba($primary-color, 0.8) 0%,
            rgba(darken($primary-color, 15%), 0.9) 100%),
        url('/mountain.jpg') center/cover no-repeat;
    z-index: 1;

    &::after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: linear-gradient(45deg,
                transparent 0%,
                rgba(255, 255, 255, 0.02) 50%,
                transparent 100%);
        animation: shimmer 4s ease-in-out infinite;
    }
}

.hero-container {
    position: relative;
    z-index: 2;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 clamp(1rem, 3vw, 2rem);
    box-sizing: border-box;
}

.hero-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: clamp(1.5rem, 4vw, 3rem);
    padding: clamp(2rem, 4vw, 3rem) clamp(1.5rem, 3vw, 2.5rem);
    background: rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(12px);
    border-radius: 24px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow:
        0 8px 32px rgba(0, 0, 0, 0.3),
        inset 0 1px 0 rgba(255, 255, 255, 0.1);
    transition: all 0.3s ease;
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;

    &:hover {
        background: rgba(255, 255, 255, 0.1);
        box-shadow:
            0 12px 40px rgba(0, 0, 0, 0.4),
            inset 0 1px 0 rgba(255, 255, 255, 0.15);
    }
}

.logo-left,
.logo-right {
    flex-shrink: 0;
}

.logo-desktop {
    height: clamp(80px, 8vw, 120px);
    width: auto;
    filter: brightness(0) invert(1) drop-shadow(0 4px 12px rgba(0, 0, 0, 0.4));
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

    &:hover {
        transform: scale(1.05) rotate(1deg);
        filter: brightness(0) invert(1) drop-shadow(0 6px 16px rgba(0, 0, 0, 0.5));
    }
}

.divider {
    width: 2px;
    height: clamp(80px, 10vh, 120px);
    background: linear-gradient(180deg,
            transparent 0%,
            rgba(255, 255, 255, 0.6) 20%,
            rgba(255, 255, 255, 0.9) 50%,
            rgba(255, 255, 255, 0.6) 80%,
            transparent 100%);
    border-radius: 1px;
    box-shadow: 0 0 8px rgba(255, 255, 255, 0.3);
    flex-shrink: 0;
}

.hero-text {
    flex: 1;
    text-align: center;
    color: white;
    min-width: 0;
    max-width: 100%;
}

.hero-title {
    font-size: clamp(2.5rem, 6vw, 2rem);
    font-weight: 800;
    margin: 0 0 1rem 0;
    letter-spacing: -0.02em;
    line-height: 0.9;
    background: linear-gradient(135deg, #ffffff 0%, #f0f8ff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    word-break: break-word;
}

.hero-subtitle {
    font-size: clamp(1.1rem, 2.8vw, 1.6rem);
    font-weight: 400;
    margin: 0;
    color: rgba(255, 255, 255, 0.95);
    line-height: 1.5;
    text-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
    letter-spacing: 0.01em;
    word-break: break-word;
}

.logos-mobile {
    display: none;
}

// Responsive Design
@media (max-width: 900px) {
    .hero-banner {
        min-height: clamp(240px, 35vh, 320px);
    }

    .hero-content {
        flex-direction: column;
        gap: clamp(1.5rem, 4vw, 2rem);
        padding: clamp(1.5rem, 3vw, 2rem);
        text-align: center;
    }

    .logo-left,
    .logo-right,
    .divider {
        display: none;
    }

    .hero-text {
        order: 1;

        .hero-title {
            margin-bottom: 0.75rem;
        }
    }

    .logos-mobile {
        display: flex;
        order: 2;
        gap: clamp(2rem, 5vw, 3rem);
        justify-content: center;
        align-items: center;
        padding: clamp(1rem, 2.5vw, 1.5rem);
        background: rgba(255, 255, 255, 0.05);
        border-radius: 16px;
        backdrop-filter: blur(8px);
        width: 100%;
        max-width: 320px;
        margin: 0 auto;
        box-sizing: border-box;
    }

    .logo-mobile {
        height: clamp(70px, 10vw, 100px);
        width: auto;
        filter: brightness(0) invert(1) drop-shadow(0 3px 8px rgba(0, 0, 0, 0.4));
        transition: all 0.3s ease;

        &:hover {
            transform: scale(1.08);
            filter: brightness(0) invert(1) drop-shadow(0 4px 12px rgba(0, 0, 0, 0.5));
        }
    }
}

@media (max-width: 480px) {
    .hero-content {
        gap: clamp(1rem, 3vw, 1.5rem);
        padding: clamp(1rem, 2.5vw, 1.5rem);
    }

    .logos-mobile {
        gap: clamp(1.5rem, 4vw, 2rem);
        padding: clamp(0.75rem, 2vw, 1rem);
        max-width: 280px;
    }

    .logo-mobile {
        height: clamp(50px, 12vw, 80px);
    }
}

// Animation shimmer
@keyframes shimmer {

    0%,
    100% {
        opacity: 0;
        transform: translateX(-100%);
    }

    50% {
        opacity: 1;
        transform: translateX(100%);
    }
}

// Desktop - masquer les logos mobiles
@media (min-width: 901px) {
    .logos-mobile {
        display: none !important;
    }
}
</style>

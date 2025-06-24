<script setup lang="ts">
import SectionPart from '../sectionPart.vue';


</script>
<template>
  <SectionPart title="Une évolution guidée par le sens et l’action">
    <template #default>
      <div class="trajectory-content">
        <div class="intro">
          <p class="intro-text">
            Issu du terrain, je me suis formé pour mieux répondre aux enjeux d’aujourd’hui : <strong>accompagner,
              innover, et
              construire des projets à impact</strong>. Chaque étape de mon parcours m’a rapproché de cette envie de
            contribuer,
            concrètement, à des initiatives qui ont du sens.
          </p>
        </div>

        <div class="timeline">
          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>8 ans chez Decathlon</h3>
              <p>
                Manager d’équipe, pilote opérationnel, formateur… j’y ai développé le sens du collectif, l’adaptabilité
                et la culture de l’action..
              </p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Développeur web</h3>
              <p>
                Je conçois et maintiens des solutions numériques pensées pour les utilisateurs, fiables et
                responsables.
              </p>
            </div>
          </div>
        </div>

        <div class="motivation">
          <h3>Pourquoi moi, maintenant ?</h3>
          <p class="motivation-intro">
            Les Jeux 2030 sont un <strong>défi unique</strong> : ils rassemblent territoire, transition écologique,
            excellence opérationnelle et engagement collectif.
          </p>

          <div class="motivation-points">
            <div class="motivation-point">
              <div class="point-icon">🏔️</div>
              <h4>Ancrage territorial</h4>
              <p>Une <strong>connaissance des Alpes</strong>, terrain de vie, de sport et d'engagement depuis
                toujours.</p>
            </div>

            <div class="motivation-point">
              <div class="point-icon">🚀</div>
              <h4>Double expertise</h4>
              <p>Une <em>vision transversale</em> alliant <strong>coordination d'équipes</strong> et <strong>solutions
                  numériques</strong>.</p>
            </div>

            <div class="motivation-point">
              <div class="point-icon">🎯</div>
              <h4>Valeurs alignées</h4>
              <p>Une philosophie en phase avec l'esprit olympique : <strong>exigence</strong>, <em>sobriété</em> et
                <strong>coopération</strong>.</p>
            </div>
          </div>

          <blockquote class="motivation-conclusion">
              J'ai la <strong>volonté</strong> et les <strong>compétences</strong>
              pour aider à construire, ici, des Jeux durables et exemplaires.
          </blockquote>
        </div>
      </div>
    </template>


  </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.trajectory-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0;
}

.intro {
  text-align: center;
  margin-bottom: var(--spacing-xl);

  .intro-text {
    font-size: clamp(1.1rem, 2.5vw, 1.25rem);
    line-height: 1.8;
    color: var(--text-primary);
    margin-bottom: var(--spacing-lg);
    font-weight: 400;
    letter-spacing: 0.01em;

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
}

.timeline {
  position: relative;
  margin: var(--spacing-xl) 0;

  &::before {
    content: '';
    position: absolute;
    left: 30px;
    top: 0;
    bottom: 0;
    width: 3px;
    background: linear-gradient(180deg,
        rgba($primary-color, 0.8) 0%,
        rgba($primary-color, 0.4) 100%);
    border-radius: 2px;
  }

  .timeline-item {
    position: relative;
    display: flex;
    align-items: flex-start;
    margin-bottom: var(--spacing-lg);
    padding-left: 80px;

    &:last-child {
      margin-bottom: 0;
    }

    .timeline-marker {
      position: absolute;
      left: 21px;
      top: 8px;
      width: 20px;
      height: 20px;
      background: $primary-color;
      border: 4px solid white;
      border-radius: 50%;
      box-shadow: 0 2px 8px rgba($primary-color, 0.3);
      z-index: 2;
    }

    .timeline-content {
      flex: 1;
      background: rgba(255, 255, 255, 0.98);
      padding: var(--spacing-lg);
      border-radius: 16px;
      border: 1px solid rgba(0, 0, 0, 0.06);
      box-shadow: 0 2px 12px rgba(0, 0, 0, 0.04);
      transition: all 0.3s ease;

      &:hover {
        transform: translateX(8px);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
      }

      h3 {
        font-size: clamp(1.3rem, 2.5vw, 1.6rem);
        font-weight: 600;
        color: var(--text-primary);
        margin: 0 0 1rem 0;
        line-height: 1.3;
        position: relative;

        &::after {
          content: '';
          position: absolute;
          bottom: -4px;
          left: 0;
          width: 40px;
          height: 3px;
          background: $primary-color;
          border-radius: 2px;
        }
      }

      p {
        font-size: clamp(1rem, 1.8vw, 1.1rem);
        line-height: 1.7;
        color: var(--text-secondary);
        margin: 0;
      }
    }
  }
}

.motivation {
  margin-top: var(--spacing-xl);
  text-align: center;
  padding: var(--spacing-xl);
  background: linear-gradient(135deg,
      rgba($primary-color, 0.08) 0%,
      rgba($primary-color, 0.03) 100%);
  border-radius: 24px;
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

  h3 {
    font-size: clamp(1.4rem, 2.8vw, 1.8rem);
    font-weight: 600;
    color: var(--text-primary);
    margin: 0 0 1.5rem 0;
    line-height: 1.3;
    position: relative;
    z-index: 1;

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

  p {
    font-size: clamp(1rem, 2vw, 1.2rem);
    line-height: 1.7;
    color: var(--text-primary);
    margin: 0;
    max-width: 800px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  .motivation-intro {
    text-align: center;
    margin-bottom: var(--spacing-xl);
    font-size: clamp(1.1rem, 2.2vw, 1.3rem);
  }

  .motivation-points {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-lg);
    margin: var(--spacing-xl) 0;
  }

  .motivation-point {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    background: rgba(255, 255, 255, 0.95);
    padding: var(--spacing-lg);
    border-radius: 16px;
    border: 1px solid rgba(0, 0, 0, 0.06);
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.04);
    transition: all 0.3s ease;

    &:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
    }

    .point-icon {
      font-size: 2.5rem;
      margin-bottom: var(--spacing-md);
      display: flex;
      align-items: center;
      justify-content: center;
      width: 80px;
      height: 80px;
      background: rgba($primary-color, 0.1);
      border-radius: 50%;
      border: 2px solid rgba($primary-color, 0.2);
    }

    h4 {
      font-size: clamp(1.2rem, 2.2vw, 1.4rem);
      font-weight: 600;
      color: var(--text-primary);
      margin: 0 0 1rem 0;
      line-height: 1.3;
    }

    p {
      font-size: clamp(0.95rem, 2vw, 1.1rem);
      line-height: 1.6;
      margin: 0;
      max-width: none;
    }
  }

  .motivation-conclusion {
    background: linear-gradient(135deg, rgba($primary-color, 0.05) 0%, rgba($primary-color, 0.1) 100%);
    border: none;
    border-left: 4px solid $primary-color;
    border-radius: 12px;
    padding: var(--spacing-lg);
    margin: var(--spacing-xl) auto 0;
    max-width: 700px;
    position: relative;
    overflow: hidden;

    &::before {
      content: '';
      position: absolute;
      top: -10px;
      left: 20px;
      font-size: 4rem;
      font-family: serif;
      color: rgba($primary-color, 0.3);
      font-weight: bold;
    }

    p {
      font-size: clamp(1.1rem, 2.2vw, 1.3rem);
      line-height: 1.6;
      margin: 0 0 var(--spacing-md) 0;
      font-style: italic;
      position: relative;
      z-index: 1;
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

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }

  to {
    opacity: 1;
    transform: translateX(0);
  }
}

// Animation d'entrée séquentielle
.timeline-item {
  animation: fadeInLeft 0.6s ease-out;
  animation-fill-mode: both;

  &:nth-child(1) {
    animation-delay: 0.1s;
  }

  &:nth-child(2) {
    animation-delay: 0.3s;
  }
}

.motivation {
  animation: fadeInLeft 0.6s ease-out 0.5s;
  animation-fill-mode: both;

  .motivation-point {
    animation: fadeInUp 0.6s ease-out;
    animation-fill-mode: both;

    &:nth-child(1) {
      animation-delay: 0.7s;
    }

    &:nth-child(2) {
      animation-delay: 0.9s;
    }

    &:nth-child(3) {
      animation-delay: 1.1s;
    }
  }

  .motivation-conclusion {
    animation: fadeInUp 0.6s ease-out 1.3s;
    animation-fill-mode: both;
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

// Responsive Design
@media (max-width: 768px) {
  .timeline {
    &::before {
      left: 20px;
    }

    .timeline-item {
      padding-left: 60px;

      .timeline-marker {
        left: 11px;
        width: 18px;
        height: 18px;
      }

      .timeline-content {
        &:hover {
          transform: translateX(4px);
        }
      }
    }
  }

  .motivation {
    text-align: left;

    .motivation-points {
      grid-template-columns: 1fr;
      gap: var(--spacing-md);
    }

    .motivation-point {
      .point-icon {
        width: 60px;
        height: 60px;
        font-size: 2rem;
      }
    }

    .motivation-conclusion {
      margin-left: var(--spacing-md);
      margin-right: var(--spacing-md);

      &::before {
        font-size: 3rem;
        top: -5px;
        left: 15px;
      }
    }
  }
}

@media (max-width: 480px) {
  .timeline {
    &::before {
      left: 15px;
    }

    .timeline-item {
      padding-left: 45px;

      .timeline-marker {
        left: 6px;
        width: 16px;
        height: 16px;
        border-width: 3px;
      }
    }
  }
}
</style>
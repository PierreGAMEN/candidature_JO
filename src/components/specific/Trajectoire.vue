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
                Responsable d'équipes, pilote opérationnel et formateur, j’y ai développé le sens du collectif,
                la capacité à m'adapter à des environnements exigeants, et une approche concrète du terrain.
              </p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker"></div>
            <div class="timeline-content">
              <h3>Développeur web</h3>
              <p>
                En reconversion, j’ai acquis de nouvelles compétences techniques pour concevoir
                et maintenir des solutions numériques utiles, en gardant toujours à l’esprit les utilisateurs,
                la fiabilité et la sobriété de ce que je construis.
              </p>
            </div>
          </div>
        </div>

        <div class="motivation">
          <h3>Pourquoi moi, maintenant ?</h3>
          <p>
            Les Jeux de 2030 représenteront un défi collectif, à la croisée de l’humain, du numérique et de
            l’environnement. Je souhaite y apporter ma double expérience – terrain et technique – et mon
            attachement profond à ce territoire. Avec pragmatisme, curiosité et esprit d’équipe, je veux
            contribuer, à ma mesure, à un projet porteur de sens et tourné vers l’avenir.
          </p>
        </div>
      </div>
    </template>


  </SectionPart>
</template>
<style scoped lang="scss">
@use '@/styles/variables' as *;

.trajectory-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0;
}

.intro {
  text-align: center;
  margin-bottom: clamp(3rem, 5vw, 4rem);

  .intro-text {
    font-size: clamp(1.1rem, 2.5vw, 1.25rem);
    line-height: 1.8;
    color: #2d3748;
    margin-bottom: var(--spacing-lg);
    font-weight: 400;
    letter-spacing: 0.01em;

    strong {
      color: $primary-color;
      font-weight: 600;
      background: linear-gradient(120deg, transparent 0%, rgba($primary-color, 0.1) 0%);
      padding: 0.1em 0.2em;
      border-radius: 4px;
    }

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
  margin: clamp(3rem, 5vw, 4rem) 0;

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
    margin-bottom: clamp(2.5rem, 4vw, 3.5rem);
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
      padding: clamp(1.5rem, 3vw, 2rem);
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
        color: #2c3e50;
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
        color: #6c757d;
        margin: 0;
      }
    }
  }
}

.motivation {
  margin-top: clamp(4rem, 6vw, 5rem);
  text-align: center;
  padding: clamp(2.5rem, 4vw, 3.5rem);
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
    color: #2c3e50;
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
    color: #2c3e50;
    margin: 0;
    max-width: 800px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
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
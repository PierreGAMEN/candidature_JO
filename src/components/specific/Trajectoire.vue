<script setup lang="ts">
import SectionPart from "../sectionPart.vue";
</script>
<template>
  <SectionPart title="Une trajectoire alpine, une énergie collective">
    <template #default>
      <div class="trajectoire-content">
        <div class="story-block">
          <div class="story-icon">🏔️</div>
          <p class="story-text">
            <strong>Né dans les Alpes</strong>, j'ai grandi entre lacs et
            sommets, au rythme des saisons et des efforts. J'ai appris tôt que
            l'engagement et la persévérance ne s'enseignent pas seulement en
            salle de classe —
            <em
              >ils se forgent sur un sentier, dans un mur d'escalade, ou au cœur
              d'une équipe</em
            >.
          </p>
        </div>

        <div class="story-block">
          <div class="story-icon">🚀</div>
          <p class="story-text">
            Après un bac sport-études en montagne, j'ai consacré
            <strong>plus de 8 ans au retail sportif chez Decathlon</strong>.
            Responsable d'équipes, formateur, pilote de projets — j'ai appris à
            écouter, à décider, à fédérer. Ces années m'ont forgé une vision :
            <em>l'excellence naît de la collaboration</em>.
          </p>
        </div>

        <div class="story-block">
          <div class="story-icon">💻</div>
          <p class="story-text">
            Puis un jour, j'ai choisi de
            <strong>réapprendre, de changer de voie, de coder</strong>. Cette
            reconversion n'était pas une fuite, mais une nouvelle montagne à
            gravir. Car derrière chaque ligne de code, il y a une histoire
            humaine à raconter.
          </p>
        </div>

        <div class="story-block highlight">
          <div class="story-icon">⭐</div>
          <p class="story-text">
            <strong
              >Aujourd'hui, je suis développeur, porteur de sens,
              leader.</strong
            ><br />
            <span class="emphasis"
              >Aujourd'hui, je veux construire pour demain.</span
            ><br />
            <span class="vision"
              >Les Jeux de 2030 représentent cette ambition : transformer les
              défis en opportunités, les rêves en réalités partagées.</span
            >
          </p>
        </div>
      </div>
    </template>
  </SectionPart>
</template>
<style scoped lang="scss">
@use "@/styles/variables" as *;

.trajectoire-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 0;
}

.story-block {
  display: flex;
  align-items: flex-start;
  gap: clamp(1rem, 3vw, 2rem);
  margin-bottom: clamp(2rem, 4vw, 3rem);
  padding: clamp(1.5rem, 3vw, 2.5rem);
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.8) 0%,
    rgba(255, 255, 255, 0.6) 100%
  );
  border-radius: 20px;
  border: 1px solid rgba($primary-color, 0.1);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(
      45deg,
      transparent 0%,
      rgba($primary-color, 0.02) 50%,
      transparent 100%
    );
    opacity: 0;
    transition: opacity 0.3s ease;
  }

  &:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.08), 0 4px 8px rgba(0, 0, 0, 0.12);

    &::before {
      opacity: 1;
    }

    .story-icon {
      transform: scale(1.1) rotate(5deg);
    }
  }

  &.highlight {
    background: linear-gradient(
      135deg,
      rgba($primary-color, 0.08) 0%,
      rgba($primary-color, 0.05) 100%
    );
    border: 2px solid rgba($primary-color, 0.2);
    box-shadow: 0 6px 25px rgba($primary-color, 0.15),
      0 2px 8px rgba($primary-color, 0.1);

    &::before {
      background: linear-gradient(
        45deg,
        transparent 0%,
        rgba($primary-color, 0.05) 50%,
        transparent 100%
      );
    }
  }
}

.story-icon {
  font-size: clamp(2rem, 4vw, 2.5rem);
  display: flex;
  align-items: center;
  justify-content: center;
  width: clamp(60px, 8vw, 80px);
  height: clamp(60px, 8vw, 80px);
  background: linear-gradient(
    135deg,
    rgba($primary-color, 0.1) 0%,
    rgba($primary-color, 0.05) 100%
  );
  border-radius: 50%;
  flex-shrink: 0;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;

  &::after {
    content: "";
    position: absolute;
    inset: -2px;
    background: linear-gradient(
      45deg,
      rgba($primary-color, 0.2) 0%,
      transparent 50%,
      rgba($primary-color, 0.2) 100%
    );
    border-radius: 50%;
    opacity: 0;
    z-index: -1;
    transition: opacity 0.3s ease;
  }

  .story-block:hover & {
    &::after {
      opacity: 1;
    }
  }
}

.story-text {
  flex: 1;
  font-size: clamp(1.1rem, 2.2vw, 1.3rem);
  line-height: 1.7;
  color: rgba($primary-color, 0.9);
  margin: 0;
  text-align: justify;
  hyphens: auto;

  strong {
    color: $primary-color;
    font-weight: 700;
    position: relative;

    &::after {
      content: "";
      position: absolute;
      bottom: -2px;
      left: 0;
      right: 0;
      height: 2px;
      background: linear-gradient(90deg, $primary-color 0%, transparent 100%);
      opacity: 0.3;
      transition: opacity 0.3s ease;
    }

    .story-block:hover & {
      &::after {
        opacity: 0.6;
      }
    }
  }

  em {
    color: rgba($primary-color, 0.8);
    font-style: italic;
    font-weight: 500;
    position: relative;

    &::before,
    &::after {
      content: '"';
      color: rgba($primary-color, 0.4);
      font-size: 1.2em;
      font-weight: 300;
    }
  }

  .emphasis {
    display: inline-block;
    font-size: 1.1em;
    font-weight: 600;
    color: $primary-color;
    margin: 0.5rem 0;
    padding: 0.25rem 0.75rem;
    background: rgba($primary-color, 0.08);
    border-radius: 8px;
    border-left: 3px solid $primary-color;
  }

  .vision {
    display: block;
    font-style: italic;
    color: rgba($primary-color, 0.7);
    margin-top: 0.75rem;
    padding-left: 1rem;
    border-left: 2px solid rgba($primary-color, 0.3);
    font-size: 0.95em;
    line-height: 1.6;
  }
}

// Animation d'entrée en scroll
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

.story-block {
  animation: fadeInUp 0.6s ease-out;

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
}

// Responsive
@media (max-width: 768px) {
  .story-block {
    flex-direction: column;
    text-align: center;
    gap: 1rem;
    margin-bottom: 2rem;
    padding: 1.5rem;

    .story-text {
      text-align: left;
    }
  }

  .story-icon {
    align-self: center;
  }
}

@media (max-width: 480px) {
  .story-block {
    padding: 1rem;
    margin-bottom: 1.5rem;
  }

  .story-text {
    font-size: 1rem;

    .emphasis {
      font-size: 1em;
      padding: 0.2rem 0.5rem;
    }
  }
}
</style>

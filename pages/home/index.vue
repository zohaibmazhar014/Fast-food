<template>
  <section class="hero">
    <div class="hero__bg">
      <div class="hero__blob hero__blob--1" />
      <div class="hero__blob hero__blob--2" />
      <div class="hero__blob hero__blob--3" />
      <div class="hero__dots" aria-hidden="true" />
    </div>

    <div class="hero__inner">
      <div class="hero__content">
        <div class="hero__badge">
          <span class="hero__stars">★★★★☆</span>
          <span class="hero__rating">4.8</span>
          <span class="hero__divider">|</span>
          <span class="hero__reviews">8K+ happy bites</span>
        </div>

        <p class="hero__tagline">Crispy, crunchy, veggie deliciousness</p>

        <h1 class="hero__title">
          <span class="hero__title-line">Burgers that</span>
          <span class="hero__title-accent">love the earth.</span>
        </h1>

        <p class="hero__desc">
          Handcrafted plant-based burgers, fresh ingredients, and flavors that make every bite count. Good for you, kind to the planet.
        </p>

        <div class="hero__cta">
          <NuxtLink to="/order" class="hero__btn hero__btn--fill">Order now</NuxtLink>
          <a href="#" class="hero__btn hero__btn--ghost">
            <span class="hero__play" aria-hidden="true">▶</span>
            See how it’s made
          </a>
        </div>
      </div>

      <div class="hero__visual">
        <div class="hero__promo">75% off first order</div>
        <div class="hero__burger" aria-hidden="true">
          <svg viewBox="0 0 200 180" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__burger-svg">
            <ellipse cx="100" cy="35" rx="70" ry="28" fill="#F5D0A9" />
            <path d="M35 45 Q100 70 165 45" stroke="#E8B88E" stroke-width="4" fill="none" />
            <rect x="45" y="50" width="110" height="12" rx="4" fill="#7CB342" />
            <rect x="40" y="62" width="120" height="10" rx="2" fill="#FFD54F" />
            <ellipse cx="100" cy="95" rx="75" ry="25" fill="#5D4037" />
            <ellipse cx="100" cy="93" rx="70" ry="22" fill="#6D4C41" />
            <rect x="50" y="105" width="100" height="8" rx="2" fill="#E57373" />
            <ellipse cx="100" cy="145" rx="72" ry="30" fill="#F5D0A9" />
            <path d="M32 135 Q100 165 168 135" stroke="#E8B88E" stroke-width="5" fill="none" />
          </svg>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  position: relative;
  min-height: calc(100vh - 80px);
  display: flex;
  align-items: center;
  overflow: hidden;
  font-family: 'Poppins', sans-serif;
}

.hero__bg {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.hero__blob {
  position: absolute;
  border-radius: 50%;
  filter: blur(60px);
  opacity: 0.5;
}

.hero__blob--1 {
  width: 500px;
  height: 500px;
  background: linear-gradient(135deg, #FFE4D1 0%, #FFCDA2 100%);
  top: -150px;
  right: -100px;
  animation: float 8s ease-in-out infinite;
}

.hero__blob--2 {
  width: 400px;
  height: 400px;
  background: linear-gradient(135deg, #FFAF68 0%, #E85D04 50%);
  bottom: -100px;
  left: -80px;
  opacity: 0.4;
  animation: float 10s ease-in-out infinite reverse;
}

.hero__blob--3 {
  width: 280px;
  height: 280px;
  background: linear-gradient(135deg, #FFF8F0 0%, #FFE4D1 100%);
  top: 50%;
  left: 30%;
  animation: float 12s ease-in-out infinite 1s;
}

@keyframes float {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(20px, -20px) scale(1.05); }
}

.hero__dots {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(#E85D04 1px, transparent 1px);
  background-size: 24px 24px;
  opacity: 0.08;
}

.hero__inner {
  position: relative;
  z-index: 1;
  max-width: 1280px;
  margin: 0 auto;
  padding: 3rem 1.5rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;

  @media (max-width: 900px) {
    grid-template-columns: 1fr;
    gap: 2.5rem;
    text-align: center;
    padding: 2rem 1rem;
  }
}

.hero__content {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;

  @media (max-width: 900px) {
    align-items: center;
  }
}

.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: rgba(255, 255, 255, 0.95);
  padding: 0.5rem 1rem;
  border-radius: 100px;
  font-size: 0.875rem;
  font-weight: 500;
  box-shadow: 0 4px 20px rgba(232, 93, 4, 0.12);
  width: fit-content;

  @media (max-width: 900px) {
    margin: 0 auto;
  }
}

.hero__stars {
  color: #E85D04;
  letter-spacing: 0.1em;
}

.hero__rating {
  color: #2D1810;
  font-weight: 600;
}

.hero__divider {
  color: #d4a574;
  font-weight: 300;
}

.hero__reviews {
  color: #E85D04;
  font-weight: 500;
}

.hero__tagline {
  font-size: 0.9375rem;
  color: #6B4423;
  font-weight: 500;
  margin: 0;
  text-transform: lowercase;
  letter-spacing: 0.02em;
}

.hero__title {
  margin: 0;
  font-size: clamp(2.25rem, 5vw, 3.75rem);
  font-weight: 800;
  line-height: 1.1;
  color: #2D1810;
  letter-spacing: -0.02em;
}

.hero__title-line {
  display: block;
}

.hero__title-accent {
  background: linear-gradient(135deg, #E85D04 0%, #DC2F02 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero__desc {
  font-size: 1rem;
  color: #5D4E37;
  line-height: 1.6;
  margin: 0;
  max-width: 420px;

  @media (max-width: 900px) {
    max-width: none;
  }
}

.hero__cta {
  display: flex;
  align-items: center;
  gap: 1rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;

  @media (max-width: 900px) {
    justify-content: center;
  }
}

.hero__btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.875rem 1.75rem;
  border-radius: 100px;
  font-weight: 600;
  font-size: 0.9375rem;
  text-decoration: none;
  transition: all 0.25s ease;

  &--fill {
    background: linear-gradient(135deg, #E85D04 0%, #DC2F02 100%);
    color: #fff;
    box-shadow: 0 8px 24px rgba(232, 93, 4, 0.35);

    &:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 32px rgba(232, 93, 4, 0.45);
    }
  }

  &--ghost {
    background: rgba(255, 255, 255, 0.9);
    color: #2D1810;
    border: 2px solid rgba(45, 24, 16, 0.15);

    &:hover {
      border-color: #E85D04;
      color: #E85D04;
    }
  }
}

.hero__play {
  font-size: 0.7em;
  opacity: 0.9;
}

.hero__visual {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;

  @media (max-width: 900px) {
    order: -1;
  }
}

.hero__promo {
  position: absolute;
  top: 0;
  right: 10%;
  background: #fff;
  color: #E85D04;
  font-weight: 700;
  font-size: 0.875rem;
  padding: 0.5rem 1rem;
  border-radius: 100px;
  box-shadow: 0 6px 20px rgba(232, 93, 4, 0.25);
  z-index: 2;

  @media (max-width: 900px) {
    right: 50%;
    transform: translateX(50%);
    top: -0.5rem;
  }
}

.hero__burger {
  position: relative;
  width: 100%;
  max-width: 380px;
  filter: drop-shadow(0 24px 48px rgba(45, 24, 16, 0.2));
}

.hero__burger-svg {
  width: 100%;
  height: auto;
}
</style>

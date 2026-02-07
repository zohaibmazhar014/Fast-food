<template>
  <header class="header">
    <div class="header__inner">
      <NuxtLink to="/" class="header__logo">
        <span class="header__logo-icon" aria-hidden="true">
          <svg viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="16" cy="8" rx="10" ry="4" fill="currentColor"/>
            <rect x="6" y="10" width="20" height="4" rx="1" fill="currentColor"/>
            <ellipse cx="16" cy="18" rx="10" ry="4" fill="currentColor"/>
          </svg>
        </span>
        <span class="header__logo-text">BURGER</span>
      </NuxtLink>

      <nav class="header__nav" aria-label="Main">
        <NuxtLink to="/" class="header__link">Home</NuxtLink>
        <NuxtLink to="/our-outlets" class="header__link">Outlets</NuxtLink>
        <NuxtLink to="/order" class="header__link header__link--emph">Order</NuxtLink>
        <NuxtLink to="/contact" class="header__link header__link--emph">Contact</NuxtLink>
      </nav>

      <div class="header__actions">
        <NuxtLink to="/order" class="header__btn">Order now</NuxtLink>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  width: 100%;
  background: rgba(253, 248, 243, 0.92);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(232, 93, 4, 0.08);
  font-family: 'Poppins', sans-serif;
}

.header__inner {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0.875rem 1.5rem;
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  gap: 1rem;
}

.header__logo {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  text-decoration: none;
  color: #2D1810;
  font-weight: 700;
  font-size: 1.25rem;
  letter-spacing: 0.04em;
  transition: color 0.2s ease;

  &:hover {
    color: #E85D04;
  }
}

.header__logo-icon {
  display: flex;
  align-items: center;
  width: 28px;
  height: 28px;
  color: #E85D04;

  svg {
    width: 100%;
    height: 100%;
  }
}

.header__logo:hover .header__logo-icon {
  color: #DC2F02;
}

.header__nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.header__link {
  color: #5D4E37;
  text-decoration: none;
  font-size: 0.9375rem;
  font-weight: 500;
  position: relative;
  padding: 0.25rem 0;
  transition: color 0.2s ease;

  &::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: 0;
    width: 0;
    height: 2px;
    background: linear-gradient(90deg, #E85D04, #DC2F02);
    border-radius: 2px;
    transition: width 0.25s ease;
  }

  &:hover {
    color: #E85D04;
  }

  &:hover::after {
    width: 100%;
  }

  &--emph {
    font-weight: 600;
    color: #2D1810;
  }
}

.header__actions {
  justify-self: end;
}

.header__btn {
  display: inline-block;
  background: linear-gradient(135deg, #E85D04 0%, #DC2F02 100%);
  color: #fff;
  font-weight: 600;
  font-size: 0.9375rem;
  padding: 0.5rem 1.25rem;
  border-radius: 100px;
  text-decoration: none;
  box-shadow: 0 4px 14px rgba(232, 93, 4, 0.3);
  transition: all 0.25s ease;

  &:hover {
    transform: translateY(-1px);
    box-shadow: 0 6px 20px rgba(232, 93, 4, 0.4);
  }
}
</style>

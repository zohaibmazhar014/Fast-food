<template>
  <footer class="footer">
    <div class="footer__top">
      <div class="footer__inner">
        <div class="footer__brand">
          <NuxtLink to="/" class="footer__logo">
            <span class="footer__logo-icon" aria-hidden="true">
              <svg viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                <ellipse cx="16" cy="8" rx="10" ry="4" fill="currentColor"/>
                <rect x="6" y="10" width="20" height="4" rx="1" fill="currentColor"/>
                <ellipse cx="16" cy="18" rx="10" ry="4" fill="currentColor"/>
              </svg>
            </span>
            BURGER
          </NuxtLink>
          <p class="footer__tagline">Burgers that love the earth. Plant-based, full of flavor.</p>
        </div>

        <div class="footer__links">
          <h4 class="footer__heading">Quick links</h4>
          <ul class="footer__list">
            <li><NuxtLink to="/" class="footer__link">Home</NuxtLink></li>
            <li><NuxtLink to="/order" class="footer__link">Order</NuxtLink></li>
            <li><NuxtLink to="/our-outlets" class="footer__link">Our outlets</NuxtLink></li>
            <li><NuxtLink to="/contact" class="footer__link">Contact</NuxtLink></li>
          </ul>
        </div>

        <div class="footer__contact">
          <h4 class="footer__heading">Get in touch</h4>
          <ul class="footer__list footer__list--contact">
            <li>
              <span class="footer__icon" aria-hidden="true">📍</span>
              <span>123 Food Street, Your City</span>
            </li>
            <li>
              <a href="tel:+1234567890" class="footer__link">📞 +1 234 567 890</a>
            </li>
            <li>
              <a href="mailto:hello@burger.com" class="footer__link">✉️ hello@burger.com</a>
            </li>
          </ul>
        </div>

        <div class="footer__social">
          <h4 class="footer__heading">Follow us</h4>
          <div class="footer__social-links">
            <a href="#" class="footer__social-link" aria-label="Instagram">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
            </a>
            <a href="#" class="footer__social-link" aria-label="Twitter">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
            </a>
            <a href="#" class="footer__social-link" aria-label="Facebook">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="footer__bottom">
      <div class="footer__inner footer__inner--bottom">
        <p class="footer__copy">© {{ new Date().getFullYear() }} Burger. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  font-family: 'Poppins', sans-serif;
  margin-top: auto;
}

.footer__top {
  background: linear-gradient(180deg, #2D1810 0%, #1a0f0a 100%);
  color: rgba(255, 255, 255, 0.9);
  padding: 3.5rem 1.5rem 2rem;
}

.footer__inner {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr 1fr;
  gap: 2.5rem;
  align-items: start;

  @media (max-width: 900px) {
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  @media (max-width: 500px) {
    grid-template-columns: 1fr;
    text-align: center;
  }
}

.footer__brand {
  @media (max-width: 500px) {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.footer__logo {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: #fff;
  font-weight: 700;
  font-size: 1.25rem;
  letter-spacing: 0.04em;
  text-decoration: none;
  margin-bottom: 0.75rem;
  transition: color 0.2s ease;

  &:hover {
    color: #FFAF68;
  }
}

.footer__logo-icon {
  display: flex;
  width: 28px;
  height: 28px;
  color: #E85D04;

  svg {
    width: 100%;
    height: 100%;
  }
}

.footer__tagline {
  font-size: 0.9375rem;
  color: rgba(255, 255, 255, 0.65);
  line-height: 1.5;
  margin: 0;
  max-width: 260px;

  @media (max-width: 500px) {
    max-width: none;
  }
}

.footer__heading {
  font-size: 0.8125rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: rgba(255, 255, 255, 0.5);
  margin: 0 0 1rem;
}

.footer__list {
  list-style: none;
  margin: 0;
  padding: 0;

  li {
    margin-bottom: 0.5rem;
  }

  &--contact li {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    font-size: 0.9375rem;

    @media (max-width: 500px) {
      justify-content: center;
    }
  }
}

.footer__link {
  color: rgba(255, 255, 255, 0.85);
  text-decoration: none;
  font-size: 0.9375rem;
  transition: color 0.2s ease;

  &:hover {
    color: #FFAF68;
  }
}

.footer__icon {
  font-size: 1rem;
}

.footer__social {
  @media (max-width: 500px) {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.footer__social-links {
  display: flex;
  gap: 0.75rem;
}

.footer__social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.08);
  border-radius: 50%;
  color: rgba(255, 255, 255, 0.8);
  transition: all 0.2s ease;

  &:hover {
    background: #E85D04;
    color: #fff;
  }

  svg {
    width: 18px;
    height: 18px;
  }
}

.footer__bottom {
  background: #1a0f0a;
  padding: 1rem 1.5rem;
}

.footer__inner--bottom {
  display: block;
}

.footer__copy {
  font-size: 0.8125rem;
  color: rgba(255, 255, 255, 0.45);
  margin: 0;
  text-align: center;
}
</style>

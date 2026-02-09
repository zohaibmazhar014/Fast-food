<template>
  <header class="header">
    <div class="container">
      <div class="header-inner">
        <div class="header-logo">
          <NuxtLink to="/" class="">
            <span>Fast Food</span>
          </NuxtLink>
        </div>
        <div class="header-menu">
          <nav class="" aria-label="Main">
            <NuxtLink to="/" class="header__link">Home</NuxtLink>
            <NuxtLink to="/our-outlets" class="header__link">Outlets</NuxtLink>
            <NuxtLink to="/order" class="header__link header__link--emph">Order</NuxtLink>
            <NuxtLink to="/contact" class="header__link header__link--emph">Contact</NuxtLink>
          </nav>
        </div>

        <div class="header-actions">
          <NuxtLink to="/order" class="header__btn">Order now</NuxtLink>
        </div>
      </div>
    </div>
  </header>
</template>

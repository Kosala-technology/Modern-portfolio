<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function closeMenu() {
  menuOpen.value = false
}
</script>

<template>
  <header class="site-header" @keydown.esc="closeMenu">
    <div class="container header-inner">
      <a href="#home" class="brand" aria-label="Kosala Lakshan home" @click="closeMenu">
        <span class="brand-mark" aria-hidden="true">k.</span>

        <span class="brand-name">
          Kosala Lakshan
          <span>Software Engineering</span>
        </span>
      </a>

      <button
        class="menu-toggle"
        type="button"
        :aria-expanded="menuOpen"
        aria-controls="main-navigation"
        @click="menuOpen = !menuOpen"
      >
        {{ menuOpen ? 'Close' : 'Menu' }}
        <span aria-hidden="true">{{ menuOpen ? '−' : '+' }}</span>
      </button>

      <nav
        id="main-navigation"
        class="navigation"
        :class="{ 'is-open': menuOpen }"
        aria-label="Main navigation"
      >
        <a href="#home" @click="closeMenu">Home</a>

        <a href="#approach" @click="closeMenu">My approach</a>

        <a href="#projects" @click="closeMenu"> Projects </a>

        <a href="#skills" @click="closeMenu"> Skills </a>

        <a href="#contact" @click="closeMenu"> Contact </a>

        <a
          class="nav-contact"
          href="https://github.com/Kosala-technology"
          target="_blank"
          rel="noopener noreferrer"
          @click="closeMenu"
        >
          GitHub <span aria-hidden="true">↗</span>
        </a>
      </nav>
    </div>
  </header>
</template>

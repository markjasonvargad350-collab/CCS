<script setup>

import { RouterLink } from 'vue-router'
import FacultyAndStaff from './FacultyandStaff.vue'
import Partnerships from './Partnerships.vue'
import Programs from './Programs.vue'
const asset = (fileName) => `/assets/${fileName}`

const navItems = [
  { label: 'Home', to: '/#hero' },
  { label: 'Programs', to: '/#programs' },
  { label: 'Faculty & Staff', to: '/#faculty' },
  { label: 'Partners', to: '/#partners' },
]



</script>

<template>

  <header class="site-header">
    <RouterLink class="brand" to="/#hero" aria-label="Go to hero section">
      <img :src="asset('ccs-logo.png')" alt="CCS logo" />
      <span>CPU CCS</span>
    </RouterLink>

    <nav class="nav-menu" aria-label="Primary navigation">
      <RouterLink v-for="item in navItems" :key="item.to" :to="item.to">
        {{ item.label }}
      </RouterLink>
    </nav>
  </header>

  <main>
    <section id="hero" class="hero-section section-block">
      <div class="hero-copy">
        <p class="eyebrow">Central Philippine University</p>
        <h1>College of Computer Studies</h1>
        <p>
          A redesigned one-page CCS mockup built to showcase computing programs,
          mentors, and partnerships.
        </p>
        <div class="hero-actions" aria-label="Hero quick links">
          <RouterLink to="/#programs">Explore Programs</RouterLink>
          <RouterLink to="/#faculty">Meet the Team</RouterLink>
        </div>
      </div>

      <div class="hero-logo-panel" aria-label="CCS identity">
        <img :src="asset('ccs-logo.png')" alt="College of Computer Studies logo" />
        <p>Remember. Connect. Engage. Build. Share.</p>
      </div>
    </section>

    <Programs />
    <FacultyAndStaff />
    <Partnerships />
  
  </main>
</template>

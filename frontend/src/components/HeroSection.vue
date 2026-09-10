<script setup>
const technologies = ['Vue.js', 'JavaScript', 'SCSS', 'Git']

const principles = [
  {
    number: '01',
    title: 'An eye for design.',
    description:
      'A multimedia background shapes how I think about layout, hierarchy, and the details that make an interface feel clear.',
  },
  {
    number: '02',
    title: 'Built to be used.',
    description:
      'I focus on responsive interfaces, reusable components, and interactions that work across different screen sizes.',
  },
  {
    number: '03',
    title: 'Always developing.',
    description:
      'Alongside frontend development, I’m learning Laravel and APIs to understand how complete web applications come together.',
  },
]
</script>

<template>
  <section id="home" class="hero" aria-labelledby="hero-title">
    <div class="container">
      <div class="hero-topline">
        <p>PERSONAL PORTFOLIO</p>
        <p>BASED IN SRI LANKA</p>
      </div>

      <div class="hero-layout">
        <div class="hero-main">
          <p class="hero-intro">Hi, I’m Kosala Lakshan.</p>

          <h1 id="hero-title">
            Thoughtful design.<br />
            <span class="accent-text">Practical code.</span>
          </h1>

          <div class="hero-summary">
            <span class="summary-rule" aria-hidden="true"></span>

            <p>
              A software engineering intern turning ideas into clear, responsive web
              experiences—with a designer’s attention to detail.
            </p>
          </div>

          <div class="hero-actions">
            <a class="button button-primary" href="#projects">
              View my work
              <span aria-hidden="true">↓</span>
            </a>

            <a class="text-link" href="#approach">
              A little about me
              <span aria-hidden="true">↓</span>
            </a>
          </div>
        </div>

        <aside class="hero-note" aria-label="Background and current focus">
          <span class="note-index">ABOUT / 01</span>

          <div class="name-composition" aria-hidden="true">
            <span class="name-line">Kosa</span>
            <span class="name-line">la<span class="name-dot">.</span></span>
          </div>

          <p class="note-caption">
            A creative perspective.<br />
            An engineering mindset.
          </p>

          <dl class="profile-details">
            <div>
              <dt>Background</dt>
              <dd>ICT · Multimedia Technology</dd>
            </div>

            <div>
              <dt>Currently exploring</dt>
              <dd>Vue.js & Laravel</dd>
            </div>
          </dl>
        </aside>
      </div>

      <div class="hero-footer">
        <div class="technology-group">
          <span class="technology-label">MY TOOLKIT</span>

          <ul class="technology-list" aria-label="Development tools">
            <li v-for="technology in technologies" :key="technology">
              {{ technology }}
            </li>
          </ul>
        </div>

        <a class="scroll-link" href="#approach">
          Get to know me
          <span aria-hidden="true">↓</span>
        </a>
      </div>
    </div>
  </section>

  <section id="approach" class="approach-section" aria-labelledby="approach-title">
    <div class="container">
      <div class="section-heading">
        <p class="section-kicker">THE WAY I THINK</p>
        <h2 id="approach-title">
          More than how it looks.<br />
          How it works, too.
        </h2>
      </div>

      <div class="approach-grid">
        <article v-for="principle in principles" :key="principle.number" class="approach-item">
          <span class="approach-number">{{ principle.number }}</span>
          <h3>{{ principle.title }}</h3>
          <p>{{ principle.description }}</p>
        </article>
      </div>
    </div>
  </section>
</template>

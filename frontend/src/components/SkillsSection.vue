<script setup>
const skillGroups = [
  {
    number: '01',
    title: 'Frontend development',
    description: 'Building responsive interfaces with reusable components and clear interactions.',
    skills: ['Vue.js', 'JavaScript', 'HTML', 'CSS / SCSS'],
  },
  {
    number: '02',
    title: 'Interface design',
    description: 'Bringing structure and clarity to the way people see and use a website.',
    skills: ['Responsive layouts', 'Typography', 'Visual hierarchy'],
  },
  {
    number: '03',
    title: 'Development tools',
    description: 'Managing source code and working with a modern frontend development setup.',
    skills: ['Git', 'GitHub', 'Vite', 'npm', 'VS Code'],
  },
]
</script>

<template>
  <section id="skills" class="skills-section" aria-labelledby="skills-title">
    <div class="container">
      <div class="skills-heading">
        <p class="section-kicker">SKILLS & TOOLS</p>

        <div>
          <h2 id="skills-title">What I build with.</h2>
          <p class="skills-introduction">
            A growing toolkit shaped by hands-on development and a background in multimedia
            technology.
          </p>
        </div>
      </div>

      <div class="skills-grid">
        <article v-for="group in skillGroups" :key="group.number" class="skill-group">
          <div class="skill-group-heading">
            <span class="skill-number">{{ group.number }}</span>
            <h3>{{ group.title }}</h3>
          </div>

          <p class="skill-description">{{ group.description }}</p>

          <ul class="skill-tags" :aria-label="group.title">
            <li v-for="skill in group.skills" :key="skill">
              {{ skill }}
            </li>
          </ul>
        </article>
      </div>

      <aside class="learning-note" aria-labelledby="learning-title">
        <p id="learning-title" class="learning-label">CURRENTLY LEARNING</p>

        <div>
          <h3>Connecting the frontend to the backend.</h3>
          <p>
            Exploring Laravel and API development, with contact form integration planned for this
            portfolio.
          </p>
        </div>

        <span class="learning-technology">Laravel / APIs</span>
      </aside>
    </div>
  </section>
</template>

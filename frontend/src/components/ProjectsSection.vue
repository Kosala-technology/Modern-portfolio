<script setup>
const projects = [
  {
    id: 'modern-portfolio',
    number: '01',
    category: 'PERSONAL PROJECT',
    title: 'Personal developer portfolio',
    description:
      'A single-page website presenting my background, development approach, and selected work.',
    contribution:
      'Designed and developed the Vue frontend with reusable components, responsive layouts, and accessible navigation.',
    technologies: ['Vue.js', 'Vite', 'SCSS'],
    status: 'In development',
    nextStep: 'Laravel integration for contact form handling.',
    repository: 'https://github.com/Kosala-technology/Modern-portfolio',
  },
]
</script>

<template>
  <section id="projects" class="projects-section" aria-labelledby="projects-title">
    <div class="container">
      <div class="projects-heading">
        <div>
          <p class="section-kicker">SELECTED WORK</p>
          <h2 id="projects-title">Ideas into interfaces.</h2>
        </div>

        <a
          class="text-link"
          href="https://github.com/Kosala-technology?tab=repositories"
          target="_blank"
          rel="noopener noreferrer"
        >
          All repositories
          <span aria-hidden="true">↗</span>
        </a>
      </div>

      <div class="project-list">
        <article
          v-for="project in projects"
          :key="project.id"
          class="project-entry"
          :aria-labelledby="`${project.id}-title`"
        >
          <div class="project-index">
            <span>{{ project.number }}</span>
            <p>{{ project.category }}</p>
          </div>

          <div class="project-content">
            <span class="project-status">{{ project.status }}</span>

            <h3 :id="`${project.id}-title`">
              {{ project.title }}
            </h3>

            <p class="project-description">
              {{ project.description }}
            </p>

            <ul class="project-technologies" aria-label="Project technologies">
              <li v-for="technology in project.technologies" :key="technology">
                {{ technology }}
              </li>
            </ul>
          </div>

          <div class="project-details">
            <h4>My contribution</h4>
            <p>{{ project.contribution }}</p>

            <h4 class="project-next-label">Planned next</h4>
            <p>{{ project.nextStep }}</p>

            <a
              class="project-source"
              :href="project.repository"
              target="_blank"
              rel="noopener noreferrer"
              :aria-label="`View source code for ${project.title} on GitHub`"
            >
              View source code
              <span aria-hidden="true">↗</span>
            </a>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

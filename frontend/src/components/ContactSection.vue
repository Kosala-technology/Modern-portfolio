<script setup>
// Add the contact details you want to display publicly.
const email = 'kosalainfor2002@gmail.com'
const linkedinUrl =
  'https://www.linkedin.com/in/kosala-lakshan-samararathna-833aa5357/?skipRedirect=true'
const githubUrl = 'https://github.com/Kosala-technology'
</script>

<template>
  <section id="contact" class="contact-section" aria-labelledby="contact-title">
    <div class="container contact-layout">
      <div class="contact-content">
        <p class="section-kicker">GET IN TOUCH</p>

        <h2 id="contact-title">
          Good work starts<br />
          with a conversation<span>.</span>
        </h2>

        <p class="contact-description">
          Have a project in mind, an opportunity to share, or an interest in my work? Let’s connect.
        </p>

        <a
          v-if="email.trim()"
          class="button button-primary contact-email-button"
          :href="`mailto:${email.trim()}`"
        >
          Say hello
          <span aria-hidden="true">↗</span>
        </a>
      </div>

      <div class="contact-links">
        <a v-if="email.trim()" class="contact-link" :href="`mailto:${email.trim()}`">
          <span class="contact-link-text">
            <span class="contact-link-label">EMAIL</span>
            <span class="contact-link-value">{{ email.trim() }}</span>
          </span>

          <span class="contact-link-arrow" aria-hidden="true">↗</span>
        </a>

        <a
          v-if="linkedinUrl.trim()"
          class="contact-link"
          :href="linkedinUrl.trim()"
          target="_blank"
          rel="noopener noreferrer"
        >
          <span class="contact-link-text">
            <span class="contact-link-label">LINKEDIN</span>
            <span class="contact-link-value">Connect professionally</span>
          </span>

          <span class="contact-link-arrow" aria-hidden="true">↗</span>
        </a>

        <a class="contact-link" :href="githubUrl" target="_blank" rel="noopener noreferrer">
          <span class="contact-link-text">
            <span class="contact-link-label">GITHUB</span>
            <span class="contact-link-value">Explore my repositories</span>
          </span>

          <span class="contact-link-arrow" aria-hidden="true">↗</span>
        </a>
      </div>
    </div>
  </section>
</template>

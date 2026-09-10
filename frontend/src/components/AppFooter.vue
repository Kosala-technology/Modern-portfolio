<script setup>
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="site-footer">
    <div class="container footer-inner">
      <a class="footer-brand" href="#home"> Kosala Lakshan<span>.</span> </a>

      <p class="footer-copyright">© {{ currentYear }} Kosala Lakshan</p>

      <a class="footer-top-link" href="#home">
        Back to top
        <span aria-hidden="true">↑</span>
      </a>
    </div>
  </footer>
</template>

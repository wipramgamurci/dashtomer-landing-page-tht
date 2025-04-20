<template>
  <footer class="w-full bg-slate-900 py-8 text-slate-100">
    <div
      class="max-w-[1200px] mx-auto px-4 md:px-12 flex flex-col md:flex-row items-center justify-between gap-4"
    >
      <div class="text-sm"> 2025 Brightly. All rights reserved.</div>
      <nav class="flex items-center gap-6">
        <a href="#" class="hover:underline text-slate-200 text-sm"
          >Privacy Policy</a
        >
        <a href="#" class="inline-flex items-center text-slate-100 hover:text-indigo-400 transition" aria-label="X (Twitter)">
          <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6">
            <title>X</title>
            <path d="M18.901 1.153h3.68l-8.04 9.19L24 22.846h-7.406l-5.8-7.584-6.638 7.584H.474l8.6-9.83L0 1.154h7.594l5.243 6.932ZM17.61 20.644h2.039L6.486 3.24H4.298Z"/>
          </svg>
        </a>
        <a href="#" class="inline-flex items-center text-slate-100 hover:text-indigo-400 transition" aria-label="LinkedIn">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-6 h-6">
            <title>LinkedIn</title>
            <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854zm4.943 12.248V6.169H2.542v7.225zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248S2.4 3.226 2.4 3.934c0 .694.521 1.248 1.327 1.248zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225z"/>
          </svg>
        </a>
      </nav>
    </div>
  </footer>
</template>

<script setup lang="ts">
// No additional logic needed for now
</script>

<style scoped>
/* All styles handled by Tailwind */
</style>

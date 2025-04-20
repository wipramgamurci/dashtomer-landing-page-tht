<template>
  <section class="w-full bg-white py-12 md:py-20">
    <div class="max-w-xl mx-auto px-4 md:px-0 text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-indigo-600 mb-4">Join the Bright Side</h2>
      <p class="text-lg text-slate-700 mb-8">Sign up for early access and help shape the future of productivity.</p>
      <form class="flex flex-col sm:flex-row gap-4 justify-center items-center" @submit.prevent>
        <label for="cta-email" class="sr-only">Email address</label>
        <input
          id="cta-email"
          type="email"
          required
          class="w-full sm:w-auto flex-1 px-5 py-3 rounded-lg border border-slate-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-100 text-base outline-none transition"
          placeholder="Enter your email"
          autocomplete="email"
        />
        <button
          type="submit"
          class="bg-indigo-600 text-white px-8 py-3 rounded-lg font-semibold text-lg shadow hover:bg-indigo-700 transition-colors focus:outline-none"
        >
          Notify Me
        </button>
      </form>
    </div>
  </section>
</template>

<script setup lang="ts">
// No additional logic needed for now
</script>

<style scoped>
/* All styles handled by Tailwind */
</style>

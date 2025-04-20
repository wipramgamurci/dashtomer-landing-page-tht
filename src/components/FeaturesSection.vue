<template>
  <section class="w-full bg-slate-50 py-12 md:py-20">
    <div class="max-w-[1200px] mx-auto px-4 md:px-12">
      <h2
        class="text-3xl md:text-4xl font-bold text-slate-900 text-center mb-10"
      >
        Features
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Feature 1 -->
        <div
          class="bg-white rounded-lg shadow p-8 flex flex-col items-center text-center"
        >
          <!-- Icon: View Boards (placeholder SVG) -->
          <svg
            class="w-12 h-12 text-indigo-600 mb-4"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
            aria-hidden="true"
            aria-label="Collaborative Boards icon"
          >
            <rect x="3" y="3" width="7" height="7" rx="1.5" />
            <rect x="14" y="3" width="7" height="7" rx="1.5" />
            <rect x="14" y="14" width="7" height="7" rx="1.5" />
            <rect x="3" y="14" width="7" height="7" rx="1.5" />
          </svg>
          <h3 class="text-xl font-semibold mb-2">Collaborative Boards</h3>
          <p class="text-slate-700">
            Organize tasks and ideas visually with real-time collaboration for
            your entire team.
          </p>
        </div>
        <!-- Feature 2 -->
        <div
          class="bg-white rounded-lg shadow p-8 flex flex-col items-center text-center"
        >
          <!-- Icon: Check Circle (placeholder SVG) -->
          <svg
            class="w-12 h-12 text-indigo-600 mb-4"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
            aria-hidden="true"
            aria-label="Goal Tracking icon"
          >
            <circle cx="12" cy="12" r="10" />
            <path d="M9 12l2 2 4-4" />
          </svg>
          <h3 class="text-xl font-semibold mb-2">Goal Tracking</h3>
          <p class="text-slate-700">
            Set, track, and celebrate goals to keep everyone aligned and
            motivated.
          </p>
        </div>
        <!-- Feature 3 -->
        <div
          class="bg-white rounded-lg shadow p-8 flex flex-col items-center text-center"
        >
          <!-- Icon: Link (placeholder SVG) -->
          <svg
            class="w-12 h-12 text-indigo-600 mb-4"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
            aria-hidden="true"
            aria-label="Seamless Integrations icon"
          >
            <path
              d="M10 13a5 5 0 0 1 7.07 0l1.41 1.41a5 5 0 0 1-7.07 7.07l-1.41-1.41"
            />
            <path
              d="M14 11a5 5 0 0 0-7.07 0l-1.41 1.41a5 5 0 0 0 7.07 7.07l1.41-1.41"
            />
          </svg>
          <h3 class="text-xl font-semibold mb-2">Seamless Integrations</h3>
          <p class="text-slate-700">
            Connect Brightly with your favorite tools for a unified workflow.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// No additional logic needed for now
</script>

<style scoped>
/* No extra styles needed; all handled by Tailwind */
</style>

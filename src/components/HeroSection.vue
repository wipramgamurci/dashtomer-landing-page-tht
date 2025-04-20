<template>
  <section class="w-full bg-white py-12 md:py-20">
    <div
      class="max-w-[1200px] mx-auto flex flex-col md:flex-row items-center px-4 md:px-12 gap-10 md:gap-16"
    >
      <!-- Text Content -->
      <div class="flex-1 text-center md:text-left">
        <h1
          class="text-4xl md:text-5xl font-bold text-indigo-600 leading-tight mb-4"
        >
          Work Brighter, Together
        </h1>
        <p class="text-xl text-slate-800 mb-8">
          Brightly helps remote teams plan, prioritize, and achieve their
          goals—without the chaos.
        </p>
        <button
          class="bg-indigo-600 text-white px-8 py-3 rounded-lg font-semibold text-lg shadow hover:bg-indigo-700 transition-colors focus:outline-none"
        >
          Get Early Access
        </button>
      </div>
      <!-- Illustration -->
      <div class="flex-1 flex justify-center md:justify-end">
        <img
          src="../assets/team-collaboration.svg"
          alt="Team collaboration illustration"
          class="w-full max-w-xs md:max-w-md rounded-lg shadow-md"
          loading="lazy"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

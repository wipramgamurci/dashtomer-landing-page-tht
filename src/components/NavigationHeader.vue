<template>
  <header class="w-full bg-white shadow-sm">
    <nav class="max-w-[1200px] mx-auto flex justify-between items-center px-4 md:px-12 py-4">
      <!-- Brand -->
      <div class="text-2xl font-bold text-indigo-600 tracking-tight">Brightly</div>
      <!-- Navigation Links -->
      <ul class="hidden md:flex gap-8 text-slate-800 font-medium">
        <li>
          <a href="#" class="hover:text-indigo-600 transition-colors">Home</a>
        </li>
        <li>
          <a href="#features" class="hover:text-indigo-600 transition-colors">Features</a>
        </li>
        <li>
          <a href="#pricing" class="hover:text-indigo-600 transition-colors">Pricing</a>
        </li>
        <li>
          <a href="#contact" class="hover:text-indigo-600 transition-colors">Contact</a>
        </li>
      </ul>
      <!-- Mobile Hamburger (placeholder only) -->
      <button class="md:hidden text-slate-800 focus:outline-none" aria-label="Open menu">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </nav>
  </header>
</template>

<script setup lang="ts">
// No logic required for static header (per requirements)
</script>

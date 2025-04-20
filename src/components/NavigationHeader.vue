<template>
  <header class="w-full bg-white shadow-sm">
    <nav class="max-w-[1200px] mx-auto flex justify-between items-center px-4 md:px-12 py-4">
      <!-- Brand -->
      <div class="text-2xl font-bold text-indigo-600 tracking-tight">Brightly</div>
      <!-- Desktop Navigation Links -->
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
      <!-- Mobile Hamburger Button -->
      <button
        class="md:hidden text-slate-800 focus:outline-none"
        aria-label="Open menu"
        @click="openMenu"
        ref="hamburgerBtn"
      >
        <svg v-if="!mobileMenuOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7 transition-all">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7 transition-all">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </nav>
    <!-- Mobile Menu Overlay -->
    <transition name="fade">
      <div
        v-if="mobileMenuOpen"
        class="fixed inset-0 z-50 bg-black/40 backdrop-blur-sm flex md:hidden"
        @click.self="closeMenu"
      >
        <nav
          class="bg-white w-4/5 max-w-xs h-full p-8 flex flex-col gap-8 shadow-xl animate-slide-in"
          ref="menuDrawer"
          tabindex="-1"
          aria-label="Mobile Navigation"
        >
          <a href="#" class="text-lg font-medium text-slate-800 hover:text-indigo-600 transition-colors" @click="closeMenu">Home</a>
          <a href="#features" class="text-lg font-medium text-slate-800 hover:text-indigo-600 transition-colors" @click="closeMenu">Features</a>
          <a href="#pricing" class="text-lg font-medium text-slate-800 hover:text-indigo-600 transition-colors" @click="closeMenu">Pricing</a>
          <a href="#contact" class="text-lg font-medium text-slate-800 hover:text-indigo-600 transition-colors" @click="closeMenu">Contact</a>
        </nav>
      </div>
    </transition>
  </header>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue';

const mobileMenuOpen = ref(false);
const menuDrawer = ref<HTMLElement | null>(null);
const hamburgerBtn = ref<HTMLButtonElement | null>(null);

function openMenu() {
  mobileMenuOpen.value = true;
  // Focus the menu when it opens
  setTimeout(() => {
    menuDrawer.value?.focus();
  }, 50);
}
function closeMenu() {
  mobileMenuOpen.value = false;
  // Return focus to hamburger after closing
  setTimeout(() => {
    hamburgerBtn.value?.focus();
  }, 50);
}

function handleKeydown(e: KeyboardEvent) {
  if (mobileMenuOpen.value && e.key === 'Escape') {
    closeMenu();
  }
  // Trap focus inside menu when open
  if (mobileMenuOpen.value && e.key === 'Tab') {
    const focusableEls = menuDrawer.value?.querySelectorAll('a');
    if (!focusableEls || focusableEls.length === 0) return;
    const first = focusableEls[0];
    const last = focusableEls[focusableEls.length - 1];
    if (e.shiftKey && document.activeElement === first) {
      e.preventDefault();
      (last as HTMLElement).focus();
    } else if (!e.shiftKey && document.activeElement === last) {
      e.preventDefault();
      (first as HTMLElement).focus();
    }
  }
}

onMounted(() => {
  window.addEventListener('keydown', handleKeydown);
});
onBeforeUnmount(() => {
  window.removeEventListener('keydown', handleKeydown);
});
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s cubic-bezier(0.4,0,0.2,1);
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
@keyframes slide-in {
  from {
    transform: translateX(-100%);
    opacity: 0.5;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}
.animate-slide-in {
  animation: slide-in 0.35s cubic-bezier(0.4,0,0.2,1);
}
</style>

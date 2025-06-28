<template>
  <section class="content-card delay-4 pixel-border-trans p-6 rounded-lg shadow-md">
    <h2 class="pixel-art-font text-3xl font-bold px-4 pb-4 pt-2 text-[var(--color-text-primary)] flex items-center gap-3">
      <span class="text-2xl">💖</span>Interests
    </h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 p-4">
      <div 
        v-for="interest in interests" 
        :key="interest.title"
        class="link-card flex flex-col items-center gap-3 rounded-lg border-2 p-4"
        :class="interest.classes"
      >
        <div class="text-5xl">{{ interest.emoji }}</div>
        <h3 class="pixel-art-font text-xl font-bold" :class="interest.titleClass">{{ interest.title }}</h3>
      </div>
    </div>
  </section>
</template>

<script setup>
const interests = [
  {
    emoji: '👾',
    title: 'Pixel Art',
    classes: 'border-[#FFCDEA] bg-[#FFF7FA]',
    titleClass: 'text-[var(--color-text-secondary)]'
  },
  {
    emoji: '🎮',
    title: 'Gaming',
    classes: 'border-[#BAE6FD] bg-[#F0F9FF]',
    titleClass: 'text-[#4A8DAC]'
  },
  {
    emoji: '🎧',
    title: 'Music',
    classes: 'border-[#FFF3CF] bg-[#FFFBEB]',
    titleClass: 'text-[#D97706]'
  }
]
</script>
<template>
  <section id="projects" class="content-card delay-2 pixel-border-trans p-6 rounded-lg shadow-md scroll-mt-24">
    <h2 class="pixel-art-font text-3xl font-bold px-4 pb-4 pt-2 text-[var(--color-text-primary)] flex items-center gap-3">
      <span class="text-2xl">💖</span>My Projects
    </h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 p-4">
      <a 
        v-for="project in projects" 
        :key="project.title"
        class="link-card block pixel-border border-2 p-4 rounded-md group"
        :class="project.borderClass"
        :style="{ background: project.background }"
        :href="project.url" 
        target="_blank"
      >
        <h3 class="pixel-art-font text-xl font-bold transition-colors" :class="project.titleClass">
          {{ project.title }}
        </h3>
        <p class="pixel-art-font text-sm transition-colors" :class="project.descClass">
          {{ project.description }}
        </p>
      </a>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'My blog ✨',
    description: 'A place where i post my stuff',
    url: 'https://blog.lunazhu.top',
    borderClass: 'border-[#D1E0FF]',
    background: 'linear-gradient(to bottom right, #E0F0FF, #D1E4FF)',
    titleClass: 'text-[var(--color-text-primary)] group-hover:text-[#C15A94]',
    descClass: 'text-[var(--color-text-secondary)] group-hover:text-[#A25092]'
  },
  {
    title: 'Coming soon! 🐾',
    description: 'Coming Soon!',
    url: '#',
    borderClass: 'border-[#D1E8FF]',
    background: 'linear-gradient(to bottom right, #F0F8FF, #E4F2FF)',
    titleClass: 'text-[#70A9D8] group-hover:text-[#5A94C1]',
    descClass: 'text-[#65A7B5] group-hover:text-[#5092A2]'
  },
  {
    title: 'Estrogen Tracker 🍥',
    description: 'An estrogen tracker.',
    url: 'https://estropad.lunazhu.top',
    borderClass: 'border-[#FFE0D1]',
    background: 'linear-gradient(to bottom right, #FFF0E0, #FFE4D1)',
    titleClass: 'text-[#D8B870] group-hover:text-[#C1A05A]',
    descClass: 'text-[#B5A765] group-hover:text-[#A29250]'
  },
  {
    title: 'LunaTodo 🗓️',
    description: 'A cutesy digital todo app.',
    url: 'https://todo.lunazhu.top',
    borderClass: 'border-[#D1FFD1]',
    background: 'linear-gradient(to bottom right, #F0FFF0, #E4FFE4)',
    titleClass: 'text-[#70D870] group-hover:text-[#5AC15A]',
    descClass: 'text-[#65B565] group-hover:text-[#50A250]'
  }
]
</script>
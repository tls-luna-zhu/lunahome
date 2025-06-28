<template>
  <section class="content-card delay-1 pixel-border-trans p-6 rounded-lg shadow-md" id="skills" ref="skillsSection">
    <h2 class="pixel-art-font text-3xl font-bold px-4 pb-4 pt-2 text-[var(--color-text-primary)] flex items-center gap-3">
      <span class="text-2xl">🛠️</span>Skills
    </h2>
    <div class="space-y-5 p-4">
      <div v-for="skill in skills" :key="skill.name">
        <div class="flex justify-between items-center mb-1">
          <p class="pixel-art-font text-[var(--color-text-secondary)] text-lg font-medium">{{ skill.name }}</p>
          <p class="pixel-art-font text-[var(--color-text-primary)] text-sm font-medium">{{ skill.level }}</p>
        </div>
        <div class="progress-bar-bg">
          <div 
            class="progress-bar-fill" 
            :style="{ 
              backgroundColor: skill.color,
              width: isVisible ? skill.width : '0%'
            }"
          ></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const skillsSection = ref(null)
const isVisible = ref(false)

const skills = [
  { name: 'Nuxt.js', level: 'Intermediate', width: '90%', color: 'var(--color-trans-pink)' },
  { name: 'Web Design (Tailwindcss)', level: 'Still learning', width: '75%', color: 'var(--color-trans-blue)' },
  { name: 'Pixel Art', level: 'Novice', width: '60%', color: '#70D870' },
  { name: 'Game Development (Godot)', level: 'Beginner', width: '40%', color: '#D8B870' }
]

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        isVisible.value = true
        observer.unobserve(entry.target)
      }
    })
  }, { threshold: 0.1 })

  if (skillsSection.value) {
    observer.observe(skillsSection.value)
  }
})
</script>
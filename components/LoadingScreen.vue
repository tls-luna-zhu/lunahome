<template>
  <div 
    v-if="!loadingComplete" 
    id="loading-screen" 
    class="fixed inset-0 z-50 flex items-center justify-center bg-gradient-to-br from-[#FAF0F7] to-[#FCEEF5] transition-opacity duration-1000"
    :class="{ 'fade-out': fadeOut }"
  >
    <div class="text-center">
      <!-- Cute Loading Icon -->
      <div class="relative mb-8">
        <div class="loading-heart w-16 h-16 mx-auto mb-4">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
            <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z" fill="url(#heartGradient)"/>
            <defs>
              <linearGradient id="heartGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" style="stop-color:#FF89B8;stop-opacity:1" />
                <stop offset="50%" style="stop-color:#F5A9B8;stop-opacity:1" />
                <stop offset="100%" style="stop-color:#5BCEFA;stop-opacity:1" />
              </linearGradient>
            </defs>
          </svg>
        </div>
        <!-- Floating sparkles around heart -->
        <div class="absolute -top-2 -left-2 w-3 h-3 sparkle-float sparkle-1">
          <svg viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
            <path d="M5 0L6.12257 3.87743L10 5L6.12257 6.12257L5 10L3.87743 6.12257L0 5L3.87743 3.87743L5 0Z" fill="#F5A9B8"/>
          </svg>
        </div>
        <div class="absolute -top-1 -right-3 w-2 h-2 sparkle-float sparkle-2">
          <svg viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
            <path d="M3 0L3.67383 2.32617L6 3L3.67383 3.67383L3 6L2.32617 3.67383L0 3L2.32617 2.32617L3 0Z" fill="#5BCEFA"/>
          </svg>
        </div>
        <div class="absolute -bottom-2 -right-1 w-2.5 h-2.5 sparkle-float sparkle-3">
          <svg viewBox="0 0 8 8" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
            <path d="M4 0L4.89442 2.89442L8 4L4.89442 5.10558L4 8L3.10558 5.10558L0 4L3.10558 2.89442L4 0Z" fill="#FF89B8"/>
          </svg>
        </div>
        <div class="absolute -bottom-1 -left-3 w-2 h-2 sparkle-float sparkle-4">
          <svg viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
            <path d="M3 0L3.67383 2.32617L6 3L3.67383 3.67383L3 6L2.32617 3.67383L0 3L2.32617 2.32617L3 0Z" fill="#F5A9B8"/>
          </svg>
        </div>
      </div>
      
      <!-- Loading Text -->
      <h2 class="pixel-art-font text-2xl font-bold text-[#D870A9] mb-4 loading-text">Loading Luna's Palace...</h2>
      
      <!-- Cute Progress Bar -->
      <div class="w-64 mx-auto">
        <div class="progress-bar-bg pixel-border-white border-2">
          <div 
            class="progress-bar-fill bg-gradient-to-r from-[#FF89B8] to-[#5BCEFA]"
            :style="{ width: progress + '%' }"
          ></div>
        </div>
      </div>
      
      <!-- Loading dots -->
      <div class="flex justify-center mt-4 space-x-1">
        <div class="loading-dot w-2 h-2 bg-[#FF89B8] rounded-full"></div>
        <div class="loading-dot w-2 h-2 bg-[#F5A9B8] rounded-full"></div>
        <div class="loading-dot w-2 h-2 bg-[#5BCEFA] rounded-full"></div>
      </div>
    </div>
  </div>
</template>

<script setup>
const loadingComplete = ref(false)
const fadeOut = ref(false)
const progress = ref(0)

onMounted(() => {
  // Simulate loading progress
  const interval = setInterval(() => {
    progress.value += Math.random() * 15
    if (progress.value >= 100) {
      progress.value = 100
      clearInterval(interval)
      
      // Start fade out after a brief delay
      setTimeout(() => {
        fadeOut.value = true
        
        // Complete loading after fade animation
        setTimeout(() => {
          loadingComplete.value = true
        }, 1000)
      }, 300)
    }
  }, 200)
  
  // Fallback: complete loading after 5 seconds
  setTimeout(() => {
    if (!loadingComplete.value) {
      progress.value = 100
      fadeOut.value = true
      setTimeout(() => {
        loadingComplete.value = true
      }, 1000)
    }
  }, 5000)
})
</script>
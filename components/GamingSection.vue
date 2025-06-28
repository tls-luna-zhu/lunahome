<template>
  <section class="content-card delay-3 pixel-border-trans p-6 rounded-lg shadow-md">
    <h2 class="pixel-art-font text-3xl font-bold px-4 pb-4 pt-2 text-[var(--color-text-primary)] flex items-center gap-3">
      <span class="text-2xl">🎮</span>Gaming Setup(Osu!)
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 p-4">
      <!-- Tablet Area -->
      <div class="flex flex-col items-center gap-4 rounded-lg border-2 border-[#FFB3D1] bg-[#FFF0F8] p-6">
        <h3 class="pixel-art-font text-[var(--color-text-secondary)] text-xl font-bold">Tablet Area</h3>
        <div class="relative">
          <!-- Tablet Visual -->
          <div class="w-36 h-24 bg-gradient-to-br from-[#E8E8E8] to-[#D0D0D0] rounded-lg border-2 border-[#B0B0B0] pixel-border-white relative">
            <!-- Full Area Highlight -->
            <div class="absolute inset-2 bg-gradient-to-br from-[#FFE0F0] to-[#FFB3D1] rounded border-2 border-[#FF89B8] opacity-80">
              <div class="absolute inset-1 border border-dashed border-[#FF66AA] rounded flex items-center justify-center">
                <span class="pixel-art-font text-xs text-[#FF66AA] font-bold">FULL</span>
              </div>
            </div>
            <!-- Tablet Brand -->
            <div class="absolute bottom-1 left-2 pixel-art-font text-xs text-[#666] font-bold">PTH-851</div>
            <!-- Dimensions -->
            <div class="absolute top-1 right-1 pixel-art-font text-xs text-[#666] font-bold">325×203mm</div>
          </div>
        </div>
        <p class="pixel-art-font text-[var(--color-text-muted)] text-sm text-center">Wacom PTH-851<br/>325.12 × 203.2 mm<br/>Full Area Usage</p>
      </div>
      
      <!-- Tapping Style -->
      <div class="flex flex-col items-center gap-4 rounded-lg border-2 border-[#BAE6FD] bg-[#F0F9FF] p-6">
        <h3 class="pixel-art-font text-[#4A8DAC] text-xl font-bold">Tapping Style</h3>
        <div class="relative">
          <!-- Keypad Visual -->
          <div class="w-28 h-16 bg-gradient-to-br from-[#F8F8F8] to-[#E0E0E0] rounded-lg border-2 border-[#C0C0C0] pixel-border-white relative">
            <!-- Keys -->
            <div class="absolute top-2 left-1 w-6 h-5 bg-gradient-to-br from-[#E0F0FF] to-[#BAE6FD] rounded border border-[#5BCEFA] flex items-center justify-center">
              <span class="pixel-art-font text-xs text-[#4A8DAC] font-bold">A</span>
            </div>
            <div class="absolute top-2 left-1/2 transform -translate-x-1/2 w-6 h-5 bg-gradient-to-br from-[#F0F0F0] to-[#D0D0D0] rounded border border-[#A0A0A0] flex items-center justify-center">
              <span class="pixel-art-font text-xs text-[#666] font-bold">S</span>
            </div>
            <div class="absolute top-2 right-1 w-6 h-5 bg-gradient-to-br from-[#E0F0FF] to-[#BAE6FD] rounded border border-[#5BCEFA] flex items-center justify-center">
              <span class="pixel-art-font text-xs text-[#4A8DAC] font-bold">D</span>
            </div>
            <!-- Finger indicators -->
            <div class="absolute -top-3 left-2 w-2 h-2 bg-[#FF89B8] rounded-full border border-white"></div>
            <div class="absolute -top-3 right-2 w-2 h-2 bg-[#FF89B8] rounded-full border border-white"></div>
            <!-- Brand -->
            <div class="absolute bottom-1 left-1 pixel-art-font text-xs text-[#666] font-bold">O3C</div>
          </div>
        </div>
        <p class="pixel-art-font text-[#4A8DAC] text-sm text-center">SayoDevice O3C<br/>Ring (A) + Index (D) Fingers</p>
      </div>
    </div>
  </section>
</template>
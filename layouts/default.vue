<template>
  <div class="bg-pink-100">
    <!-- Loading Screen -->
    <LoadingScreen />
    
    <!-- Animated Sparkle Background -->
    <div class="sparkle-bg"></div>

    <div class="main-content relative flex size-full min-h-screen flex-col group/design-root show">
      <div class="flex h-full grow flex-col">
        <!-- Header -->
        <AppHeader />

        <!-- Main Content -->
        <main class="px-4 sm:px-8 md:px-16 lg:px-24 flex flex-1 justify-center py-10 sm:py-16">
          <slot />
        </main>
      </div>
    </div>
  </div>
</template>
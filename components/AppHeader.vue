<template>
  <header class="header shadow-md">
    <div class="top-bar-trans-flag">
      <div class="trans-flag-stripe trans-blue"></div>
      <div class="trans-flag-stripe trans-pink"></div>
      <div class="trans-flag-stripe trans-white"></div>
      <div class="trans-flag-stripe trans-pink"></div>
      <div class="trans-flag-stripe trans-blue"></div>
    </div>
    <nav class="flex items-center justify-between px-4 sm:px-10 py-3">
      <div class="flex items-center gap-4">
        <div class="size-8 text-[var(--color-accent-pink)]">
          <svg fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M2 2H4V4H2V2ZM4 2H6V4H4V2ZM6 2H8V4H6V2ZM8 2H10V4H8V2ZM10 2H12V4H10V2ZM12 2H14V4H12V2ZM14 2H16V4H14V2ZM16 2H18V4H16V2ZM18 2H20V4H18V2ZM20 2H22V4H20V2ZM2 4H4V6H2V4ZM20 4H22V6H20V4ZM2 6H4V8H2V6ZM6 6H8V8H6V6ZM10 6H14V8H10V6ZM16 6H18V8H16V6ZM20 6H22V8H20V6ZM2 8H4V10H2V8ZM8 8H10V10H8V8ZM14 8H16V10H14V10ZM20 8H22V10H20V8ZM2 10H4V12H2V10ZM6 10H8V12H6V10ZM10 10H14V12H10V10ZM16 10H18V12H16V10ZM20 10H22V12H20V10ZM2 12H4V14H2V12ZM20 12H22V14H20V12ZM2 14H4V16H2V14ZM4 14H6V16H4V14ZM6 14H8V16H6V14ZM8 14H10V16H8V14ZM10 14H12V16H10V14ZM12 14H14V16H12V14ZM14 14H16V16H14V14ZM16 14H18V16H16V14ZM18 14H20V16H18V14ZM20 14H22V16H20V14Z"/>
          </svg>
        </div>
        <h2 class="pixel-art-font text-[var(--color-text-primary)] text-2xl font-bold">Luna's Palace</h2>
      </div>
      <div class="flex items-center gap-4 sm:gap-6">
        <div class="hidden sm:flex items-center gap-6">
          <a class="nav-link pixel-art-font text-lg font-medium" href="#about">About</a>
          <a class="nav-link pixel-art-font text-lg font-medium" href="#projects">My Projects</a>
          <a class="nav-link pixel-art-font text-lg font-medium" href="#contact">Contact</a>
        </div>
        <div class="avatar rounded-md size-12 pixel-border border-2 border-[var(--color-border-pink)]" style='background-image: url("/avatar.png");'></div>
      </div>
    </nav>
  </header>
</template>
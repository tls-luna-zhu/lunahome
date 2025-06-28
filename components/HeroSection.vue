<template>
  <section class="flex justify-center">
    <div class="hero-card flex w-full max-w-lg flex-col gap-6 items-center bg-white pixel-border-trans p-8 rounded-lg shadow-lg">
      <div class="avatar rounded-md min-h-40 w-40 pixel-border border-4 border-[var(--color-border-pink)]" style='background-image: url("/avatar.png");'></div>
      <div class="flex flex-col items-center justify-center gap-1">
        <h1 class="pixel-art-font trans-gradient-text text-6xl font-bold text-center pb-2">Luna</h1>
        <p class="pixel-art-font text-[var(--color-text-secondary)] text-xl font-medium text-center">Gamer, developer & Student</p>
        <p class="pixel-art-font text-[var(--color-text-secondary)] text-lg font-normal text-center">She/Her</p>
        <div class="flex gap-3 mt-4">
          <a class="primary-button px-5 py-2.5 rounded-md pixel-border-white border-2 text-sm font-bold flex items-center gap-2" href="https://github.com/tls-luna-zhu" rel="noopener noreferrer" target="_blank">
            <svg viewBox="0 0 24 24" width="20" height="20" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M0 2H2V0H4V2H6V4H4V6H2V4H0V2ZM2 8H4V6H6V8H8V6H10V8H8V10H6V12H4V10H2V8ZM6 14H4V12H2V14H0V16H2V18H4V16H6V14Z M10 10H8V12H10V14H8V16H10V18H12V20H14V22H16V20H18V22H20V20H22V18H24V16H22V14H20V16H18V14H16V12H14V10H12V8H14V6H16V4H18V2H20V0H18V2H16V0H14V2H12V4H10V6H12V8H10V10ZM16 16H14V18H16V16ZM18 10H16V8H18V6H20V8H22V10H20V12H18V10Z" fill="white"></path>
            </svg>
            GitHub
          </a>
          <a class="osu-button px-5 py-2.5 rounded-md pixel-border-white border-2 text-sm font-bold flex items-center gap-2" href="https://osu.ppy.sh/users/36748073" rel="noopener noreferrer" target="_blank">
            <svg viewBox="0 0 24 24" width="20" height="20" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="12" cy="12" r="10" fill="white"/>
              <circle cx="12" cy="12" r="6" fill="none" stroke="#FF66AA" stroke-width="2"/>
              <circle cx="12" cy="12" r="2" fill="#FF66AA"/>
            </svg>
            Osu!
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
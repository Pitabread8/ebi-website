<!-- to-do: make it responsive (hamburger for mobile) -->

<template>
  <header>
    <nav>
      <ul
        class="flex w-full flex-row items-center justify-center gap-8 px-8 py-6 text-lg font-serif"
      >
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/blog">Blog</NuxtLink></li>
        <li><NuxtLink to="/events">Events</NuxtLink></li>
        <li><NuxtLink to="/contact">Contact</NuxtLink></li>
      </ul>
    </nav>
  </header>
</template>

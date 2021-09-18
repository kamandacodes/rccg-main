<template>
  <div class="text-gray-900">

    <!-- Header & Navigation -->
    <header class="bg-purple-900 p-6 flex flex-col md:flex-row items-center justify-between text-center">
      <img src="/rccg.png" width="90px" />
      <nav class="flex gap-x-4 text-gray-600">
        <g-link class="nav__link text-white hover:text-red-500" to="/">Home</g-link>
        <g-link class="nav__link" to="/blog/">Blog</g-link>
      </nav>
    </header>

    <!-- Page Content -->
    <main class="p-6 min-h-screen">
      <slot/>
    </main>
    <footer class="bg-purple-900 p-6 flex flex-col md:flex-row items-center justify-between text-center">
      <img src="/rccg.png" width="90px" />
      <nav class="flex gap-x-4 text-gray-600">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/blog/">Blog</g-link>
      </nav>

    </footer>

  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style scoped>
/* Add any Global Styles Here */

.active--exact { /* Active Nav Link */
  @apply text-gray-900;
}
</style>
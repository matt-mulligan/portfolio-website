<template>
  <div class="grid grid-cols-[20%_1fr] min-h-screen">
    <aside class="bg-gray-900 text-white p-4">
      <h2 class="text-xl font-semibold mb-6">Matt Mulligan</h2>

      <nav class="space-y-2">
        <NuxtLink to="/" class="block hover:bg-gray-800 rounded p-2">
          Bio
        </NuxtLink>
      </nav>
    </aside>

    <main class="p-8 bg-gray-50">
      <slot />
    </main>
  </div>
</template>

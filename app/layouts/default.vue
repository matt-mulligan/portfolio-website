<script setup lang="ts">
const links = [
  { label: 'About', to: '/' },
  { label: 'Experience', to: '/experience' },
  { label: 'Education', to: '/education' },
  { label: 'Skills', to: '/skills' },
]
</script>

<template>
  <div class="template-layout">

    <aside class="template-sidebar">
      <div class="sb-spacing-top"></div>

      <div class="sb-content">
        <NuxtImg
            class="profile-pic"
            format="jpg"
            src="/profile_picture.jpg"
            alt="Look at that handsome devil!"
        >
        </NuxtImg>
        <NuxtLink
            v-for="link in links"
            :key="link.to"
            :to="link.to"
            class="nav-link"
        >
          {{ link.label }}
        </NuxtLink>
      </div>

      <div class="sb-spacing-bottom"></div>
    </aside>

    <main class="template-content">
      <slot />
    </main>
  </div>
</template>

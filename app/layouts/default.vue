<script setup lang="ts">
  const route = useRoute();
  const isMenuOpen = ref(false);

  const links = [
    { label: 'About', to: '/' },
    { label: 'Experience', to: '/experience' },
    { label: 'Education', to: '/education' },
    { label: 'Skills', to: '/skills' },
  ];

  watch(
    () => route.path,
    () => {
      isMenuOpen.value = false;
    },
  );
</script>

<template>
  <div class="template-layout">
    <aside class="template-sidebar">
      <div class="sb-spacing-top"></div>

      <div class="sb-content">
        <div class="sb-header">
          <NuxtImg
            class="profile-pic"
            format="jpg"
            src="/profile_picture.jpg"
            alt="Portrait of Matt Mulligan"
          />

          <button
            class="menu-toggle"
            type="button"
            aria-controls="primary-navigation"
            :aria-expanded="isMenuOpen"
            :aria-label="isMenuOpen ? 'Close navigation menu' : 'Open navigation menu'"
            @click="isMenuOpen = !isMenuOpen"
          >
            <span class="menu-toggle-line"></span>
            <span class="menu-toggle-line"></span>
            <span class="menu-toggle-line"></span>
          </button>
        </div>

        <nav id="primary-navigation" class="sb-navigation" :class="{ 'is-open': isMenuOpen }">
          <NuxtLink v-for="link in links" :key="link.to" :to="link.to" class="nav-link">
            {{ link.label }}
          </NuxtLink>
        </nav>
      </div>

      <div class="sb-spacing-bottom"></div>
    </aside>

    <main class="template-content">
      <slot />
    </main>
  </div>
</template>

<script setup lang="ts"></script>

<template>
  <div class="template-layout">
    <aside class="template-sidebar">
      <div class="sb-spacing-top">SPACING TOP</div>
      <div class="sb-img">
        <NuxtImg
          class="profile-pic"
          format="jpg"
          src="/profile_picture.jpg"
          alt="Look at that handsome devil!"
        >
        </NuxtImg>
      </div>
      <div class="sb-nav">NAV</div>
      <div class="sb-spacing-bottom">SPACING BOTTOM</div>
    </aside>
    <main class="template-content">
      <slot />
    </main>
  </div>
</template>

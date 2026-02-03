<script setup lang="ts"></script>

<template>
  <div class="layout">
    <aside class="sidebar">
      <div class="sb-spacing-top">SPACING TOP</div>
      <div class="sb-img">
        <NuxtImg class="profile-pic" format="jpg" src="/profile_picture.jpg"> </NuxtImg>
      </div>
      <div class="sb-nav">NAV</div>
      <div class="sb-spacing-bottom">SPACING BOTTOM</div>
    </aside>
    <main class="content">
      <slot />
    </main>
  </div>
</template>

<style>
  /* Page-Level Container Grid */
  .layout {
    display: grid;
    grid-template-rows: 100vh;
    grid-template-columns: 18vw 82vw;
    grid-template-areas: 'sidebar content';
  }

  /* Main Element Grids */
  .sidebar {
    grid-area: sidebar;
    background-color: darkolivegreen;

    display: grid;
    grid-template-rows: 1.5fr 2fr 5fr 1.5fr;
    grid-template-columns: 1fr;
    grid-template-areas:
      'sb-spacing-top'
      'sb-img'
      'sb-nav'
      'sb-spacing-bottom';

    border: 3px solid red;
  }

  .content {
    grid-area: content;
    border: 3px solid blue;
  }

  /* Child Sidebar Classes */
  .sb-spacing-top {
    grid-area: sb-spacing-top;
    border: 3px solid black;
  }

  .sb-img {
    grid-area: sb-img;
    border: 3px solid black;
    justify-items: center;
    align-items: center;
  }

  .profile-pic {
    border-radius: 50%;
    max-block-size: 200px;
  }

  .sb-nav {
    grid-area: sb-nav;
    border: 3px solid black;
  }

  .sb-spacing-bottom {
    grid-area: sb-spacing-bottom;
    border: 3px solid black;
  }
</style>

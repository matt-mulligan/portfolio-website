<script setup lang="ts">
  defineProps<{
    heading: string;
    sections: {
      subtitle: string;
      details: string[];
    }[];
  }>();
</script>

<template>
  <article class="skills-entry">
    <h2 class="section-title">{{ heading }}</h2>

    <section v-for="section in sections" :key="section.subtitle" class="skills-section">
      <h3 class="section-subtitle">{{ section.subtitle }}</h3>

      <ul class="skills-details">
        <li v-for="detail in section.details" :key="detail" class="text-body">
          {{ detail }}
        </li>
      </ul>
    </section>
  </article>
</template>

<style scoped>
  .skills-entry:not(:last-child) {
    margin-bottom: 3rem;
  }

  .skills-section:not(:last-child) {
    margin-bottom: 2rem;
  }

  .skills-section .section-subtitle {
    margin-bottom: 0.5rem;
  }

  .skills-details {
    list-style-type: disc;
    margin: 0;
    padding-left: 1.5rem;
  }

  .skills-details .text-body {
    margin-bottom: 0.35rem;
  }
</style>

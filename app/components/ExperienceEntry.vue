<script setup lang="ts">
  defineProps<{
    jobTitle: string;
    company: string;
    startDate: string;
    endDate: string;
    details: string[];
  }>();
</script>

<template>
  <article class="experience-entry">
    <div class="experience-heading">
      <h2 class="section-title">{{ jobTitle }}</h2>
      <p class="entry-dates">{{ startDate }} &ndash; {{ endDate }}</p>
    </div>
    <p class="section-subtitle">{{ company }}</p>

    <ul class="experience-details">
      <li v-for="detail in details" :key="detail" class="text-body">
        {{ detail }}
      </li>
    </ul>
  </article>
</template>

<style scoped>
  .experience-entry:not(:last-child) {
    margin-bottom: 3rem;
  }

  .experience-heading {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 2rem;
    width: 100%;
  }

  .experience-details {
    list-style-type: disc;
    margin: 0;
    padding-left: 1.5rem;
  }

  .experience-details .text-body {
    margin-bottom: 0.35rem;
  }

  @media (max-width: 700px) {
    .experience-heading {
      align-items: flex-start;
      flex-direction: column;
      gap: 0.35rem;
    }
  }
</style>

<script setup lang="ts">
  defineProps<{
    heading: string;
    subtitle: string;
    startDate: string;
    endDate: string;
    details: string[];
  }>();
</script>

<template>
  <article class="education-entry">
    <div class="education-heading">
      <h2 class="section-title">{{ heading }}</h2>
      <p class="entry-dates">{{ startDate }} &ndash; {{ endDate }}</p>
    </div>
    <p class="section-subtitle">{{ subtitle }}</p>

    <ul class="education-details">
      <li v-for="detail in details" :key="detail" class="text-body">
        {{ detail }}
      </li>
    </ul>
  </article>
</template>

<style scoped>
  .education-entry:not(:last-child) {
    margin-bottom: 3rem;
  }

  .education-heading {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 2rem;
    width: 100%;
  }

  .education-details {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .education-details .text-body {
    margin-bottom: 0.35rem;
  }

  @media (max-width: 700px) {
    .education-heading {
      align-items: flex-start;
      flex-direction: column;
      gap: 0.35rem;
    }
  }
</style>

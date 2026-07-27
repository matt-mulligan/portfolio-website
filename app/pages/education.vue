<script setup lang="ts">
  const educationEntries = [
    {
      heading: 'University of Technology Sydney',
      subtitle: 'Bachelor of Science in Information Technology',
      startDate: 'February 2012',
      endDate: 'September 2014',
      details: [
        'Majors: Business Information Systems Management - Internetworking and Applications',
        'Graduated with Distinction',
      ],
    },
  ];
</script>

<template>
  <div>
    <h1 class="page-title">Education</h1>

    <EducationEntry
      v-for="entry in educationEntries"
      :key="`${entry.heading}-${entry.subtitle}`"
      v-bind="entry"
    />
  </div>
</template>

<script setup lang="ts">
  const experienceEntries = [
    {
      jobTitle: 'Chief Software Engineer',
      company: 'Private Consultancy',
      startDate: 'June 2025',
      endDate: 'June 2026',
      details: [
          'Led the design and delivery of a secure data encryption and sharing platform featuring end-to-end quantum-safe encryption and a zero-trust, server-knowledge architecture',
          'Developed client-specific data pipeline solutions supporting metadata-driven builds and cross-platform compilation across major cloud providers and leading big data frameworks'
      ],
    },
    {
      jobTitle: 'Lead Platform Engineer',
      company: 'Westpac - Azure Big Data Framework Team',
      startDate: 'December 2021',
      endDate: 'May 2025',
      details: [
        'Led a team of 10 software engineers delivering enterprise-grade data platform capabilities to more than 1,100 engineers across the organisation',
        'Architected and delivered a greenfield, cloud-native big data framework on Westpac\'s target-state Azure platform',
        'Increased engineering productivity by simplifying metadata models and introducing more flexible, reusable pipeline architecture',
        'Designed and built automated migration tooling that assist converting more than 12,000 legacy data pipelines to the new metadata framework',
        'Delivered average processing performance improvements exceeding 20% across big data workloads compared with the legacy platform',
        'Implemented new detailed auditing and monitoring capabilities to provide real-time visibility into data pipeline performance and health',
      ],
    },
    {
      jobTitle: 'Framework Engineer',
      company: 'Westpac - HDP Big Data Framework Team',
      startDate: 'May 2018',
      endDate: 'November 2021',
      details: [
        'Contributed to the development of Westpac\'s first enterprise Hadoop-based big data platform for large-scale data ingestion and transformation',
        'Designed and implemented field-level encryption capabilities, securing more than 400 TB of sensitive enterprise data throughout the platform\'s lifecycle',
        'Built DevSecOps deployment pipelines using Jenkins, reducing deployment times by more than 95% through automation',
        'Introduced automated functional testing for both local and cluster execution, significantly improving software quality, stability, and release confidence'
      ],
    },
    {
      jobTitle: 'Technical Lead',
      company: 'Westpac - Data Visualisation Team',
      startDate: 'February 2017',
      endDate: 'April 2018',
      details: [
        'Managed enterprise Qlikview environments for business users to consume and produce reporting'
      ],
    },
    {
      jobTitle: 'Technology Graduate',
      company: 'Westpac - Various Teams',
      startDate: 'February 2015',
      endDate: 'January 2017',
      details: [],
    },
  ];
</script>

<template>
  <div>
    <h1 class="page-title">Experience</h1>

    <ExperienceEntry
      v-for="entry in experienceEntries"
      :key="`${entry.company}-${entry.jobTitle}-${entry.startDate}`"
      v-bind="entry"
    />
  </div>
</template>

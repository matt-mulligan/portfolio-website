<script setup lang="ts"></script>

<template>
  <div>
    <h1 class="hero-title">
      <span class="text-primary">Matt </span>
      <span class="text-secondary">Mulligan</span>
    </h1>

    <p class="hero-subtitle">
      <span class="text-primary">Sydney, Australia - </span>
      <a class="text-secondary" href="mailto:matt@mattmulligan.net">matt@mattmulligan.net</a>
    </p>

    <p class="text-body">
      Software engineer with 11+ years experience working with Python, Spark and Go
    </p>
    <p class="text-body">
      Passionate about building scalable and maintainable enterprise-grade software using Test
      Driven Development
    </p>
    <p class="text-body">
      Expertise in building and optimising Big Data workflows and ecosystems from the table level up
      to entire data platforms architectures
    </p>
    <p class="text-body">
      Cloud computing and DevSecOps experience working with Azure, AWS and Github Actions
    </p>

    <div class="social-links">
      <NuxtLink to="https://github.com/matt-mulligan" target="_blank" aria-label="GitHub">
        <Icon name="simple-icons:github" class="social-icon" />
      </NuxtLink>

      <NuxtLink
        to="https://www.linkedin.com/in/matt-mulligan/"
        target="_blank"
        aria-label="LinkedIn"
      >
        <Icon name="simple-icons:linkedin" class="social-icon" />
      </NuxtLink>

      <NuxtLink to="mailto:matt@mattmulligan.net" aria-label="Email">
        <Icon name="mdi:email-outline" class="social-icon" />
      </NuxtLink>
    </div>
  </div>
</template>

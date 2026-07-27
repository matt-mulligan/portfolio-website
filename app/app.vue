<script setup lang="ts">
  const routeOrder = ['/', '/experience', '/education', '/skills'];
  const router = useRouter();

  const removeTransitionGuard = router.beforeEach((to, from) => {
    const fromIndex = routeOrder.indexOf(from.path);
    const toIndex = routeOrder.indexOf(to.path);

    if (fromIndex === -1 || toIndex === -1 || fromIndex === toIndex) return;

    to.meta.pageTransition = {
      name: toIndex > fromIndex ? 'page-swoop-down' : 'page-swoop-up',
      mode: 'out-in',
    };
  });

  onBeforeUnmount(removeTransitionGuard);
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

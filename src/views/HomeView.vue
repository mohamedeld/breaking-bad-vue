<script setup>
import BreakingCards from '@/components/BreakingCards.vue'
</script>

<template>
  <main>
    <h1>HERO</h1>
    <Suspense>
      <template #default>
        <BreakingCards />
      </template>
      <template #fallback>
        <div>
          <p>Loading...</p>
        </div>
      </template>
    </Suspense>
  </main>
</template>

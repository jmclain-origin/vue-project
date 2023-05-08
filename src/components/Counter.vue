<script setup lang="ts">
import { ref } from 'vue'
import type { Ref } from 'vue'
const count: Ref<number> = ref(0)
</script>
<template>
    <div class="text-center p-4 bg-slate-400 max-w-7xl mx-auto">
      <h1 class="text-3xl font-bold mb-4">Simple counter</h1>
      <button @click="count++" class="button">Increment</button>
      <span class="text-2xl p-3 border border-zinc-600 rounded-md mx-2 bg-zinc-800 text-zinc-50"
        >Count: {{ count }}</span
      >
      <button @click="count--" class="button">Decrement</button>
    </div>
</template>
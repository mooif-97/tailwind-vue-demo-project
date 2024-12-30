<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
    <div class="card">
        <div class="card-back-deco rounded-dashed-border">
            Card-back
        </div>
    </div>
</template>

<style scoped>
.rounded-dashed-border {
    @apply border-dashed border-4 border-cyan-400 rounded-l;
}
.card {
    @apply w-auto h-48 bg-slate-100 p-2 cursor-pointer rounded-dashed-border;
}
.card-back-deco {
    @apply p-2 h-auto text-center;
}
</style>

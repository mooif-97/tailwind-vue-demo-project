<script setup lang="ts">
import { ref } from 'vue'
import Card from "./Card.vue"

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
    <div class="card-grid">
        <card />
        <card />
        <card />
        <card />
        <card />
        <card />
        <card />
    </div>
</template>

<style scoped>
.card-grid {
    @apply grid grid-cols-1 gap-2;
}

@screen sm {
    .card-grid {
        @apply grid grid-cols-2 gap-2;
    }
}

@screen md {
    .card-grid {
        @apply grid grid-cols-3 gap-3;
    }
}

@screen lg {
    .card-grid {
        @apply grid grid-cols-4 gap-3;
    }
}

@screen xl {
    .card-grid {
        @apply grid grid-cols-6 gap-4;
    }
}
</style>

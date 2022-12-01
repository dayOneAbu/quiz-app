<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
</script>
<template>
    <div>
        this is the quiz page{{ route.params.id }}
    </div>
</template>
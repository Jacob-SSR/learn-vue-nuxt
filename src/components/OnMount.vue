<script setup>
import { onMounted, ref } from 'vue';


const month = ref('January')

onMounted(()=>{
    month.value = 'February'
})
</script>

<template>
    <p>Month: {{ month }}</p>
</template>
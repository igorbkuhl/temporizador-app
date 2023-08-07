<template>
   <span>
        <slot></slot>
   </span> 
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'Message'
});
</script>

<style scoped>

</style>
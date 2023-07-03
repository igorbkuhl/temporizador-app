<template>
    <PlayButton />
    <PauseButton />
    <StopButton />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PlayButton from '@/components/PlayButton.vue'
import PauseButton from '@/components/PauseButton.vue'
import StopButton from '@/components/StopButton.vue'

export default defineComponent({
    name: 'Controls',
    components: {
        PlayButton,
        PauseButton,
        StopButton
    }
})
</script>

<style scoped>

</style>
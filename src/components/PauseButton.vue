<template>
    <button>
        <span class="icon">
            <i class="fas fa-pause"></i>
        </span>
        <span>Pause</span>
    </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'PauseButton'
})
</script>

<style scoped>
button {
    cursor: pointer;
    padding: 20px 40px;
}

button span {
    margin: 5px;
}
</style>
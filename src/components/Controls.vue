<template>
    <!-- $emit envia os comandos play, pause e stop para o MadCounter -->
    <button @click="$emit('play'), changeStatus('running')" :disabled="isRunning">
        <span class="icon">
            <i class="fas fa-play"></i>
        </span>
        <span>Play</span>
    </button>
    <button @click="$emit('pause'), changeStatus('paused')" :disabled="isPaused">
        <span class="icon">
            <i class="fas fa-pause"></i>
        </span>
        <span>Pause</span>
    </button>
    <button @click="$emit('stop'), changeStatus('stopped')" :disabled="!isRunning && !isPaused">
        <span class="icon">
            <i class="fas fa-stop"></i>
        </span>
        <span>Stop</span>
    </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Controls',
    emits: ['play', 'pause', 'stop'],
    data() {
        return {
            isRunning: false,
            isPaused: false
        }
    },
    methods: {
        changeStatus(status: string) {
            console.log(`O novo estado do contador é ${status}`);
            switch(status) {
                case 'running':
                    this.isRunning = true
                    this.isPaused = false
                    break;
                case 'paused':
                    this.isRunning = false
                    this.isPaused = true
                    break;
                case 'stopped':
                    this.isRunning = false
                    this.isPaused = false
                    break;
                default:
                    // throw emite um erro propositalmente
                    throw new Error("Estado desconhecido: " + status);
            }
        }
    }
});
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
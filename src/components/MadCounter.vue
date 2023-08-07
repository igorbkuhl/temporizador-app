<template>
    <aside>
        <Controls @play="start()" @stop="finish()" @pause="wait()"/>
    </aside>
    <section>
        <div id="counter">Contador: <span id="counterValue">{{ counterValue }}</span></div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Controls from '@/components/Controls.vue';

export default defineComponent({
    name: 'MadCounter',
    components: {
        Controls
    },
    data() {
        return {
            counterId: 0,
            counterValue: 0
        }
    },
    methods: {
        start() {
            console.log("Iniciando.");
            this.counterId = setInterval(() => { this.counterValue++ }, 1000); // O parâmetro é dado em milisegundos.
        },
        wait() {
            console.log("Pausando.");
            clearInterval(this.counterId);
        },
        finish() {
            console.log("Finalizando.");
            clearInterval(this.counterId);
            this.counterValue = 0;
        }
    }
});
</script>

<style scoped>
#counter {
    background-color: #EEE;
    border-radius: 3px;
    margin: 3px;
    padding: 20px;
    text-align: center;
}
#counterValue {
    font-weight: bold;
}
section {
    margin: 30px;
    width: 433px;
}
</style>
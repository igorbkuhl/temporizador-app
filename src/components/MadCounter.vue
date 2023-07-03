<template>
    <aside>
        <Controls />
    </aside>
    <section>
        <div id="counter">Contador: <span id="counterValue">1</span></div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Controls from '@/components/Controls.vue'

export default defineComponent({
    name: 'MadCounter',
    components: {
        Controls
    }
});
</script>

<style scoped>

</style>
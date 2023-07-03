<template>
    <aside>
        <Controls />
    </aside>
    <section>
        <CounterArea />
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Controls from '@/components/Controls.vue'
import CounterArea from '@/components/CounterArea.vue'

export default defineComponent({
    name: 'MadCounter',
    components: {
        Controls,
        CounterArea
    }
});
</script>

<style scoped>
#counter {
    background-color: beige;
}
</style>
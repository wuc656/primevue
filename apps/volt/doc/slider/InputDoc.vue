<template>
    <DocSectionText v-bind="$attrs">
        <p>Slider is connected to an input field using two-way binding.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <div class="w-56">
            <InputText v-model.number="value" class="w-full mb-4" />
            <Slider v-model="value" class="w-full" />
        </div>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import InputText from '@/volt/InputText.vue';
import Slider from '@/volt/Slider.vue';
import { ref } from 'vue';

const value = ref(50);

const code = ref(`
<div class="card flex justify-center">
    <div class="w-56">
        <InputText v-model.number="value" class="w-full mb-4" />
        <Slider v-model="value" class="w-full" />
    </div>
</div>

<script setup lang="ts">
import InputText from '@/volt/InputText.vue';
import Slider from '@/volt/Slider.vue';
import { ref } from 'vue';

const value = ref(50);
<\/script>
`);
</script>

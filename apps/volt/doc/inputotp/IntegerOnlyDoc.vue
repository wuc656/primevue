<template>
    <DocSectionText v-bind="$attrs">
        <p>When <i>integerOnly</i> is present, only integers can be accepted as input.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <InputOtp v-model="value" integerOnly />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import InputOtp from '@/volt/InputOtp.vue';
import { ref } from 'vue';

const value = ref(null);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <InputOtp v-model="value" integerOnly />
    </div>
</template>

<script setup lang="ts">
import InputOtp from '@/volt/InputOtp.vue';
import { ref } from 'vue';

const value = ref(null);
<\/script>
`);
</script>

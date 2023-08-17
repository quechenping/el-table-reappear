<!-- @format -->

<template>
  <div>{{ msg }}</div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import type { ElTable } from 'element-plus';

interface Props {
  msg: string;
}

withDefaults(defineProps<Props>(), {});

const tableRef = ref<InstanceType<typeof ElTable>>();

defineExpose({ tableRef });
</script>

<style scoped></style>

<script setup lang="ts">
const boardSize = 10;

function numtoletter(num: number): string {
  return String.fromCharCode(96 + num);
}
</script>

<template>
  <div>
    <div
      v-for="row in boardSize"
      key="row"
      style="display: flex; background-color: pink"
    >
      {{ numtoletter(row) }}
      <div
        v-for="col in boardSize"
        key="col"
        style="flex: 1; width: 50px; height: 50px; border: 1px solid #ccc"
      >
        {{ col }}
      </div>
    </div>
  </div>
</template>

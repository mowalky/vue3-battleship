<script setup lang="ts">
const boardSize = 10;

function numtoletter(num: number): string {
  return String.fromCharCode(96 + num);
}
</script>

<template>
  <div>
    <div style="display: flex; margin-left: 50px">
      <div
        v-for="header in boardSize"
        style="flex: 1; width: 50px; height: 50px"
      >
        {{ header }}
      </div>
    </div>
    <div v-for="row in boardSize" key="row" style="display: flex">
      <div
        style="
          display: flex;
          align-items: center;
          justify-content: center;
          width: 50px;
          height: 50px;
        "
      >
        {{ numtoletter(row) }}
      </div>
      <div
        v-for="col in boardSize"
        key="col"
        style="flex: 1; width: 50px; height: 50px; border: 1px solid #ccc"
      >
        {{ numtoletter(row) + col }}
      </div>
    </div>
  </div>
</template>

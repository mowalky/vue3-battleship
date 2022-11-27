<script setup lang="ts">
const boardSize = 10;

function numtoletter(num: number): string {
  return String.fromCharCode(96 + num);
}
</script>

<template>
  <div>
    <div style="display: flex; margin-left: 52px">
      <div
        v-for="header in boardSize"
        key="header"
        style="
          display: flex;
          align-items: center;
          justify-content: center;
          width: 50px;
          height: 50px;
          border: 1px solid #ccc;
        "
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
          border: 1px solid #ccc;
        "
      >
        {{ numtoletter(row) }}
      </div>
      <div
        v-for="col in boardSize"
        key="col"
        style="
          display: flex;
          justify-content: center;
          align-items: center;
          width: 50px;
          height: 50px;
          border: 1px solid #ccc;
        "
      >
        {{ numtoletter(row) + col }}
      </div>
    </div>
  </div>
</template>

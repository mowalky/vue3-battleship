<script setup lang="ts">
const boardSize = 10;

function numtoletter(num: number): string {
  return String.fromCharCode(96 + num);
}
</script>

<template>
  <div
    style="
      background-image: url('https://st2.depositphotos.com/3768069/5426/i/950/depositphotos_54265481-stock-photo-water-seamless-texture-tile.jpg');
    "
  >
    <div v-for="row in boardSize" key="row" style="display: flex">
      <div
        v-for="col in boardSize"
        :key="numtoletter(row) + col"
        style="
          display: flex;
          justify-content: center;
          align-items: center;
          width: 50px;
          height: 50px;
          border: 1px solid white;
        "
      >
        {{ numtoletter(row) + col }}
      </div>
    </div>
  </div>
</template>

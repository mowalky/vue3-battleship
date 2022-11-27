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
      border: 4px solid #ccc;
      box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.5);
      margin-bottom: 20px;
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
  <div
    style="
      background-image: url('https://st2.depositphotos.com/3768069/5426/i/950/depositphotos_54265481-stock-photo-water-seamless-texture-tile.jpg');
      border: 4px solid #ccc;
      box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.5);
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

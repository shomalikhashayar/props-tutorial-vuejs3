<template>
  <div class="child-container">
    <h2>Access Parent Data from Child Component | Vue.js 3</h2>
    <div class="items" v-for="items in data" :key="items">
      <p>{{ items.firstName }}</p>
      <p>{{ items.lastName }}</p>
      <p>{{ items.age }}</p>
      <p>{{ items.gender }}</p>
      <p>{{ items.jobTitle }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["data"]);
</script>

<style>
.child-container h2 {
  text-align: center;
}

.items {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  font-size: 16px;
  font-weight: 600;
  color: rgb(103, 103, 103);
}

@media screen and (max-width: 480px) {
  .items {
    font-size: 14px;
  }
}

.child-container h2 {
  font-size: 22px;
  padding: 0 40px;
  line-height: 35px;
}
</style>

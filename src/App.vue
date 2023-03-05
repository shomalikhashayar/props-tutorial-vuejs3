<!-- This is our Parent Component -->
<template>
  <div class="parent-container">
    <div class="image">
      <img src="@/assets/Khashayar-Shomali.jpg" alt="Khashayar Shomali" />
    </div>
    <div class="data">
      <ChildComponent :data="data" />
    </div>
  </div>
</template>

<script setup>
import { reactive } from "vue";
import ChildComponent from "./components/ChildComponent.vue";

const data = reactive([
  {
    firstName: "Khashayar",
    lastName: "Shomali",
    age: 23,
    gender: "Male",
    jobTitle: "Front-End Developer",
  },
]);
</script>

<style>
* {
  font-family: sans-serif;
}

body {
  background-color: rgb(224, 255, 252);
}

.image {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
  margin-bottom: 50px;
}

.image img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  border: 2px solid;
  box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.988), 0 0 20px 0 rgba(0, 0, 0, 0.3);
}

@media screen and (max-width: 480px) {
  .image img {
    width: 150px;
    height: 150px;
  }
}
</style>

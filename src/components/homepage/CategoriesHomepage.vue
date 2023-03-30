<script setup>
// tanda ./ menunjukkan di dalam folder yang sama
// tanda ../ file keluar dari folder homepage
import { ref } from "vue";
import CategoriesCard from "./../CategoriesCard.vue";

const items = ref([
  { id: 1, title: "Mobile UI Kit", count: 731, image: "categories-1.jpg" },
  { id: 2, title: "Mobile UI Kit", count: 731, image: "categories-2.jpg" },
  { id: 3, title: "Mobile UI Kit", count: 731, image: "categories-3.jpg" },
  { id: 4, title: "Mobile UI Kit", count: 731, image: "categories-4.jpg" },
]);
</script>


<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <CategoriesCard
        v-for="item in items"
        :key="item.id"
        :title="item.title"
        :count="item.count"
        :image="item.image"
      />
    </div>
  </div>
</template>
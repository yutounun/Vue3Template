<script setup lang="ts">
const props = defineProps({
  placeholder: String,
  options: Array,
});
console.log(props.options);
const smallAdd = "/icons/SmallAdd.svg";
</script>

<template>
  <div class="flex items-center">
    <select class="select select-bordered w-5/6 text-gray-3">
      <option disabled selected class="text-gray-2">
        {{ props.placeholder }}
      </option>
      <template v-for="option in options" :key="option">
        <option>{{ option }}</option>
      </template>
    </select>
    <img :src="smallAdd" alt="" class="ml-5" />
  </div>
</template>

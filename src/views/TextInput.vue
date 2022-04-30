<template>
  <div class="flex max-w-full">
    <label class="grow shrink-0" v-if="label" for="{{name}}">{{ label }}</label>
    <input class="px-2 shrink border-b border-black max-w-full w-full" id="{{name}}" type="text" name="{{name}}">
  </div>
</template>
<script>
export default {
  name: "text-input",
  props: ["name", "label"]
};
</script>
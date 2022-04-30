<template>
  <div class="flex grow">
    <div v-for="value in values" class="grow">
      <input :id="name+value" :value="value" class="sr-only" :name="name" type="radio">
      <label :for="name+value" :class="labelClasses"
             class="border border-black flex items-center justify-center text-sm font-medium uppercase sm:flex-1 cursor-pointer focus:outline-none">
        <span class="font-extrabold text-gray-400" :class="textClass">
          {{ value }}
        </span>
      </label>
    </div>
  </div>
</template>
<script>
export default {
  name: "stat-selector",
  props: ["name", "size", "overrideValues"],
  computed: {
    values() {
      if (this.overrideValues?.length > 0) {
        return this.overrideValues;
      }
      return ["-1", "+1", "+2", "+3", "+4"];
    },
    sizeClass() {
    },
    labelClasses(value) {
      // 'bg-gray-300': value === '-1', paddingClass
      let classes = [];
      if (value === "-1") {
        classes.push("bg-gray-300");
      }
      if (this.size === "xs") {
        classes.push("px-1");
      } else if (this.size === "sm") {
        classes.push("px-1");
      } else {
        classes.push("py-1");
      }
      return classes.join(" ");
    },
    textClass() {
      if (this.size === "xs") {
        return "text-xs";
      }
      if (this.size === "sm") {
        return "text-sm";
      }
      return "text-lg";
    }
  }
};
</script>
<template>
  <div>
    <h4 class="font-bold">{{ label }}</h4>
    <div class="flex" :class="{'pl-10': !noPadding}">
      <stat-selector :size="size" :label="label" :name="name"></stat-selector>
      <div class="resize-none border border-black text-gray-500 flex p-1"
           :class="{'text-xs': size === 'xs'}">
        roll:
        <span class="font-bold" :class="{'text-xs': size === 'xs'}">{{ roll }}</span>
      </div>
    </div>
  </div>
</template>
<script>
import StatSelector from "@/views/StatSelector.vue";

export default {
  name: "skill-selector",
  components: { StatSelector },
  props: ["name", "size", "label", "noPadding"],
  computed: {
    roll() {
      return 4;
    }
  }
};
</script>
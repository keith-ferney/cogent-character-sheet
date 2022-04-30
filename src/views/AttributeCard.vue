<template>
  <div>
    <span class="flex gap-1 items-baseline"><h4 class="font-bold">{{ abbreviatedTitle }}</h4><small>{{ title }}</small></span>
    <stat-selector :name="name" />
    <small>
      {{ helpText }}
    </small>
  </div>
</template>
<script>
import StatSelector from "@/views/StatSelector.vue";

export default {
  name: "attribute-card",
  components: { StatSelector },
  props: ["title", "abbreviatedTitle", "name", "helpText"]
};
</script>
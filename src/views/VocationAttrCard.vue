<template>
  <div class="flex flex-col gap-2">
    <text-input :name="['[',name,']','name'].join()" :label="label" />
    <div class="flex justify-center gap-2 w-1/2 mx-auto">
      <stat-selector :size="size" :label="label" :name="['[',name,']','type'].join()"
                     :override-values="['str','ref', 'int']"></stat-selector>
    </div>
    <skill-selector :no-padding="true" :size="size" :name="['[',name,']','attr'].join()" />
  </div>
</template>
<script>
import SkillSelector from "@/views/SkillSelector.vue";
import TextInput from "@/views/TextInput.vue";
import StatSelector from "@/views/StatSelector.vue";

export default {
  name: "vocation-attr-card",
  props: ["name", "size", "label"],
  components: { SkillSelector, TextInput, StatSelector }
};
</script>
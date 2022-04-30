<template>
  <div>
    <vocation-attr-card :name="name" label="Vocation" />
    <div class="grid grid-cols-2 grid-rows-2 gap-4">
      <vocation-attr-card :name="[name,'][skill1'].join()" label="Skill" size="xs" />
      <vocation-attr-card :name="[name,'][skill2'].join()" label="Skill" size="xs" />
      <vocation-attr-card :name="[name,'][skill3'].join()" label="Skill" size="xs" />
      <vocation-attr-card :name="[name,'][skill4'].join()" label="Skill" size="xs" />
    </div>
  </div>
</template>
<script>
import VocationAttrCard from "@/views/VocationAttrCard.vue";

export default {
  name: "vocation-card",
  props: ["name"],
  components: { VocationAttrCard }
};
</script>
<template>
  <div>
    <h4 class="w-full text-center"><strong>{{ skillType }}</strong> Based Skills</h4>
    <slot />
  </div>
</template>
<script>

export default {
  name: "skill-card",
  props: ["skillType"]
};
</script>
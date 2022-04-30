<template>
  <div>
    <h4 class="font-bold text-lg w-full text-center">Injuries:</h4>
    <table>
      <tbody>
      <tr class="h-10">
        <td colspan="6">
          <stat-selector name="injury_level" :override-values="['1','2','3','4','5','6']"></stat-selector>
        </td>
      </tr>
      </tbody>
      <tfoot>
      <tr>
        <td colspan="6" class="text-center">
          When the level of injury exceeds your <b>BASE ROLL</b><br />
          <b>(3) + ATTRIBUTE POINTS</b>, you fall unconscious.
        </td>
      </tr>
      </tfoot>
    </table>
    <h4 class="font-bold text-lg w-full text-center">Lingering Injuries:</h4>
    <table class="table-auto">
      <thead>
      <tr>
        <th>Injury:</th>
        <th class="w-24">Penalty:</th>
      </tr>
      </thead>
      <tbody>
      <tr class="h-10" v-for="i in 6">
        <th></th>
        <th></th>
      </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
import StatSelector from "@/views/StatSelector.vue";

export default {
  name: "injury-card",
  components: { StatSelector }
};
</script>
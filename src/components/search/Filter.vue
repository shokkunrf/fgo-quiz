<template>
  <div class="filter">
    <table>
      <tr v-for="filter in filters" :key="filter">
        <td>{{ filter.name }}:</td>
        <td class="column">
          <FilterList :items="filter.items" />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import FilterList from "@/components/search/FilterList";
import { classes, rarities } from "@/constants/ServantFeatures";

export default {
  components: {
    FilterList,
  },
  data() {
    return {
      filters: [
        {
          name: "星",
          items: rarities,
        },
        {
          name: "クラス",
          items: classes,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.column {
  text-align: left;
}
</style>

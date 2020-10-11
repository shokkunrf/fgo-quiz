<template>
  <div class="filter">
    <table>
      <tr v-for="filter in filters" :key="filter">
        <td>{{ filter.name }}:</td>
        <td class="column">
          <ul class="list">
            <li v-for="item in filter.items" :key="item">
              {{ item }}
            </li>
          </ul>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import { classes, rarities } from "@/constants/ServantFeatures";

export default {
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
.list {
  display: inline-flex;
  flex-wrap: wrap;
  list-style: none;
  margin-block-start: 0;
  margin-block-end: 0;
  padding-inline-start: 0;
  > li {
    display: inline;
    font-size: 0.8rem;
    border: 1px solid #000;
    border-radius: 1rem;
    margin: 0.1rem 0.2rem;
    padding: 0.3rem;
  }
}
</style>

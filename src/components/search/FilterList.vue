<template>
  <ul class="list">
    <li v-for="item in items" :key="item">
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  props: ["items"],
};
</script>

<style lang="scss" scoped>
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

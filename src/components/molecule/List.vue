<template>
  <div class="movie-list-container">
    <div
      class="movie-list-item"
      v-for="(item, index) in dataList"
      :key="index"
      v-on:click="onItemSelected(item)"
    >
      <ListItem :title="item.title" :selected="item.id == selectedId" />
    </div>
  </div>
</template>

<script>
import ListItem from "@/components/atom/ListItem.vue";
export default {
  name: "ListData",
  components: {
    ListItem,
  },
  props: {
    dataList: Array,
    selectedId: String,
  },
  data() {
    return {
      selectedItemId: this.selectedId,
    };
  },
  methods: {
    onItemSelected(itemData) {
      this.$emit("on-item-selected", itemData);
    },
  },
};
</script>

<style scoped>
.movie-list-item {
  height: 30px;
}
.movie-list-container {
  background-color: #ececec;
  height: 100%;
  padding-top: 1em;
  width: 100%;
  display: flex;
  flex-direction: column;
}
</style>

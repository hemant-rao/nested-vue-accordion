<template>
  <div
    class="accordion accordion-flush"
    :class="[item.children ? 'have-child' : 'no-child']"
    v-for="(item, index) in items"
    :key="index"
  >
    <button
      v-if="item.title && item.children"
      type="button"
      class="accordion-button"
      :class="{ collapsed: !activeIndexes.includes(index) }"
      data-bs-toggle="collapse"
      :data-bs-target="`#collapse${index + 1}`"
      :aria-expanded="activeIndexes.includes(index)"
      :aria-controls="`collapse${index + 1}`"
      @click="toggleContent(index)"
    >
      {{ item.title }}
    </button>
    <div class="content-style" v-else>{{ item.title }}</div>
    <div
      class="accordion-collapse accordion-content"
      :class="[
        { collapse: !activeIndexes.includes(index) },
        item.children ? 'have-child' : 'no-child',
      ]"
      :id="`collapse${index + 1}`"
      v-if="activeIndexes.includes(index)"
    >
      <template v-if="item.children">
        <nested-vue-accordion :items="item.children" />
      </template>
      <div class="content-style" v-else>{{ item.title }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MultilevelAccordion",
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      activeIndexes: [],
      accordionId: "",
    };
  },
  methods: {
    toggleContent(index) {
      const currentIndex = this.activeIndexes.indexOf(index);
      if (currentIndex !== -1) {
        this.activeIndexes.splice(currentIndex, 1);
      } else {
        this.activeIndexes.push(index);
      }
    },
    dynamicIdGenerate() {
      let id = "id" + Math.random().toString(16).slice(2);
      this.accordionId = id;
      return this.accordionId;
    },
  },
};
</script>
<style scoped>
@import url("nested-vue-accordion/assets/accordion.css");

.accordion {
  /* display: flex;
    flex-direction: column; */
  margin: 0;
  padding: 0;
}

.accordion-button {
  border: none;
  cursor: pointer;
  padding: 16px 18px;
  text-align: left;
  width: 100%;
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
  transition: 0.3s;
}
.accordion-button[aria-expanded="true"] {
  background-color: #f3f3f3;
}
.accordion-button:hover {
  opacity: 0.8;
}
.accordion-button:focus {
  box-shadow: none;
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
}
.accordion-content {
  padding: 0 0 0 18px;
  transition: max-height 0.3s ease-in-out;
}
.content-style {
  padding: 16px 18px;
  border: 1px solid #ddd;
  margin-top: 15px;
  margin-bottom: 15px;
  display: flex;
  max-width: 200px;
  max-height: 200px;
}
.have-child .no-child {
  display: inline-block;
  margin-right: 15px;
}
</style>nested-vue-accordiona/src/MultilevelAccordion.vue

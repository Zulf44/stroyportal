<template>
  <div class="wrapper">
    <header-panel></header-panel>
    <path-panel></path-panel>
    <product-name></product-name>
    <product-options></product-options>
    <product-block></product-block>
  </div>
</template>

<script>
import HeaderPanel from "@/components/HeaderPanel";
import PathPanel from "./components/PathPanel.vue";
import ProductName from "./components/ProductName.vue";
import ProductOptions from "./components/ProductOptions.vue";
import ProductBlock from "./components/ProductBlock.vue";

export default {
  components: {
    HeaderPanel,
    PathPanel,
    ProductName,
    ProductOptions,
    ProductBlock,
  },
};
</script>

<style lang="scss">
.wrapper {
  width: 1280px;
  height: 786px;
  margin: 0 auto;
}

.app-wrapper {
  height: 100%;
  width: 1110px;
  margin: 0 auto;
}
</style>
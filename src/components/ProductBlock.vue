<template>
  <div class="product">
    <div class="product_wrapper">
      <product-photo></product-photo>
      <product-description></product-description>
      <product-price></product-price>
    </div>
  </div>
</template>

<script>
import ProductPhoto from "@/components/ProductPhoto";
import ProductDescription from "@/components/ProductDescription";
import ProductPrice from "@/components/ProductPrice";
export default {
  components: {
    ProductPhoto,
    ProductDescription,
    ProductPrice,
  },
};
</script>

<style lang="scss" scoped>
.product {
  padding-top: 32px;
  height: 600px;
  background-color: #fff;
}
.product_wrapper {
  display: flex;

  width: 1110px;
  margin: 0 auto;
  height: 100%;
}
</style>
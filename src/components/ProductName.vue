<template>
  <div class="product-name">
    <div class="product-name__wrapper">
      <h1 class="product-name__title">
        Штукатурка цементная цокольная Knauf Sockelpultz 25 кг
      </h1>
      <a href="#" class="product-name__share-link">
        <img
          class="product-name__share-link__img"
          src="@/assets/share.svg"
          alt=""
        />
      </a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.product-name {
  background-color: #fff;
  height: 60px;
  &__wrapper {
    width: 1110px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: start;
  }
  &__title {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 700;
    font-size: 28px;
    line-height: 38px;
    color: #050f19;
  }
  &__share-link {
    &__img {
      margin-left: 12px;
    }
  }
}
</style>
<template>
  <div class="path">
    <div class="path-wrapper">
      <div class="product-cotegory">
        <div class="product-cotegory__name">Каталог</div>
        <div class="product-cotegory__amount">4 442 521</div>
      </div>

      <div class="product-cotegory">
        <div class="product-cotegory__name">Строительные материалы</div>
        <div class="product-cotegory__amount">4 442 512 предложения</div>
      </div>
      <div class="product-cotegory">
        <div class="product-cotegory__name">Сухие строительные смеси</div>
        <div class="product-cotegory__amount">4 442 512 предложения</div>
      </div>
      <div class="product-cotegory">
        <div class="product-cotegory__name">Шпатлевки</div>
        <div class="product-cotegory__amount">4 442 512 предложения</div>
      </div>
      <div class="product-cotegory">
        <div class="product-cotegory__name">Шпатлевка Knauf</div>
        <div class="product-cotegory__amount"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.path-wrapper {
  width: 1110px;
  margin: 0 auto;
  display: flex;
}
.path {
  background-color: #fff;
  width: 100%;
  height: 80px;
}
.product-cotegory {
  margin-right: 50px;
  position: relative;
  display: flex;
  flex-direction: column;

  align-items: flex-start;
  margin-top: 16px;
  justify-content: start;
  &:last-child {
    &::before {
      display: none;
    }
  }
  &__name {
    display: flex;
    align-items: center;

    height: 20px;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    color: #050f19;
  }
  &__amount {
    display: flex;
    align-items: center;
    height: 20px;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 12px;
    color: #708598;
  }
  &::before {
    content: "";
    position: absolute;
    background: url("../assets/arrow_down.svg") 0 0 / cover no-repeat;
    width: 18px;
    height: 18px;

    background-size: cover;
    fill: #a48686;
    top: 10px;
    right: -30px;
    transform: rotate(270deg);
  }
}
</style>
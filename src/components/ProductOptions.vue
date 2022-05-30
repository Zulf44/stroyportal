<template>
  <div class="product-options-wrapper">
    <div class="product-options">
      <button class="product-options__left-btn">
        <img
          class="product-options__left-btn__img"
          src="../assets/arrow_down.svg"
          alt=""
        />
      </button>
      <div class="product-option">Где купить</div>
      <div class="product-option">Описание</div>
      <div class="product-option">Характеристики</div>
      <div class="product-option">Динамика цен</div>
      <div class="product-option">Календарь низких цен</div>
      <div class="product-option">Сравнение</div>
      <button class="product-options__right-btn">
        <img
          class="product-options__right-btn__img"
          src="../assets/arrow_down.svg"
          alt=""
        />
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scoped>
.product-options {
  position: relative;
  width: 1110px;
  height: 48px;
  background: #fafbfc;

  border: 1px solid #eceff1;
  border-radius: 4px;
  display: flex;

  &__left-btn {
    background: #fafbfc;
    height: 100%;
    width: 48px;
    overflow: hidden;
    &__img {
      transform: rotate(90deg);
    }
  }

  &__right-btn {
    right: 0;
    position: absolute;
    background: #fafbfc;
    height: 100%;
    width: 48px;
    overflow: hidden;
    border-left: 1px solid #eceff1;
    &__img {
      transform: rotate(270deg);
    }
  }
}
.product-option {
  font-family: "Open Sans", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;

  /* text */

  color: #050f19;

  padding: 12px 38px;
  height: 100%;
  display: flex;
  align-items: center;
  border-left: 1px solid #eceff1;
}
.product-options-wrapper {
  background-color: #fff;
  margin: 0 auto;
  display: flex;
  justify-content: center;
}
</style>
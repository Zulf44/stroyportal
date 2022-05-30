<template>
  <div class="price">
    <div class="price__popular-offer">Популярное предложение</div>
    <div class="price__product">
      <div class="price__product__number">39 900</div>
      <div class="price__product__currency">РУБ/ ШТ</div>
    </div>
    <div class="price__availability">В наличии</div>
    <button class="price__go">Перейти в магазин</button>
    <div class="price__provider">
      <div class="price__provider__rep">Проверенный поставщик</div>
      <div class="price__provider__name">ООО ВсеИнструменты.ру</div>
    </div>
    <div class="diler">Дилер</div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.price {
  font-family: "Open Sans", sans-serif;
  padding: 0 24px;
  margin-left: 36px;
  box-sizing: border-box;
  width: 350px;
  height: 341px;
  left: 845px;
  top: 330px;
  background: #ffffff;
  border: 1px solid #eceff1;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.03);
  border-radius: 4px;
  border-top: 4px solid #fed83d;
  &__popular-offer {
    position: relative;
    margin-top: 29px;
    margin-left: 28px;
    font-family: "Open Sans", sans-serif;
    font-weight: 600;
    font-size: 10px;
    text-transform: uppercase;
    color: #050f19;
    &::before {
      content: "";
      background: url("../assets/star.svg") 0 0 / cover no-repeat;
      width: 20px;
      height: 20px;
      position: absolute;
      left: -30px;
      top: -6px;
      background-size: cover;
    }
  }
  &__product {
    display: flex;
    margin-top: 32px;
    height: 32px;
    align-items: end;
    &__number {
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: 700;
      font-size: 28px;
      color: #050f19;
    }
    &__currency {
      margin-left: 8px;
      font-family: "Open Sans", sans-serif;
      font-weight: 600;
      font-size: 14px;
      color: #050f19;
    }
  }
  &__availability {
    margin-top: 12px;
    font-family: "Open Sans", sans-serif;

    font-weight: 600;
    font-size: 10px;

    letter-spacing: 0.04em;
    text-transform: uppercase;

    color: #05b169;
  }
  &__go {
    margin-top: 44px;
    font-family: "Open Sans", sans-serif;
    width: 302px;
    height: 48px;

    background: #fed83d;
    border-radius: 4px;

    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    line-height: 24px;

    color: #0a0a0a;
  }
  &__provider {
    position: relative;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    margin-top: 35px;
    height: 42px;
    width: 179px;
    &__rep {
      text-align: left;
      font-weight: 600;
      font-size: 10px;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: #05b169;
      margin-bottom: 12px;
    }
    &__name {
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: 600;
      font-size: 14px;

      color: #0a0a0a;
    }
    &::before {
      content: "";
      background: url("../assets/guard.svg") 0 0 / cover no-repeat;
      width: 48px;
      height: 48px;
      position: absolute;
      left: -58px;
      top: -6px;
      background-size: cover;
    }
    &::after {
      content: "";
      background: url("../assets/vse.svg") 0 0 / cover no-repeat;
      width: 42px;
      height: 20px;
      position: absolute;
      right: -60px;
      top: -6px;
      background-size: cover;
    }
  }
  .diler {
    margin-top: 9px;
    margin-left: 62px;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 7px 12px;
    gap: 10px;
    width: 60px;
    height: 20px;

    background: #e5fff0;
    border-radius: 2px;
    font-family: "Open Sans";
    font-style: normal;
    font-weight: 600;
    font-size: 10px;
    line-height: 10px;

    letter-spacing: 0.04em;
    text-transform: uppercase;

    /* green */

    color: #05b169;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
  }
}
</style>
<template>
  <div class="description">
    <div class="description__short">
      <div class="description__short__title">Коротко о таваре</div>
      <div class="parameter">
        <div class="parameter__kay">Вес</div>
        <div class="parameter__value">25—50 кг</div>
      </div>
      <div class="parameter">
        <div class="parameter__kay">Основа</div>
        <div class="parameter__value">Гипсовая супер штукатурка Knauf S..</div>
      </div>
      <a href="" class="description__all">Все хараетеристики</a>
      <div class="description__demand">Пользуется спросом</div>
      <div class="wde">
        <div class="description__views">2 274 просмотров</div>
        <div class="description__orders">602 заказа</div>
      </div>
      <div class="description__availability">
        В наличии в Москве на 4 марта 2020
      </div>
      <div class="description__offers">140 предложений</div>
      <img src="@/assets/knauf_logo.png" alt="" class="description__logo" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.description {
  padding-left: 30px;
  margin-left: 30px;
  width: 345px;
  height: 352px;
  background-color: rgb(255, 255, 255);
  &__short {
    font-family: "Open Sans", sans-serif;
    &__title {
      margin-top: 5px;
      position: relative;
      margin-bottom: 12px;
      font-style: normal;
      font-weight: 600;
      font-size: 14px;
      color: #050f19;
      &::before {
        content: "";
        background: url("../assets/file-text.svg") 0 0 / cover no-repeat;
        width: 20px;
        height: 20px;
        position: absolute;
        left: -32px;
        top: -5px;
        background-size: cover;
      }
    }
  }
  &__all {
    margin-top: 20px;
    font-size: 14px;
    color: #1652f0;
  }
  &__demand {
    margin-top: 30px;
    position: relative;

    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    color: #050f19;
    &::before {
      content: "";
      background: url("../assets/like.svg") 0 0 / cover no-repeat;
      width: 20px;
      height: 20px;
      position: absolute;
      left: -30px;
      top: -5px;
      background-size: cover;
    }
  }
  &__views {
    margin-right: 16px;
    font-weight: 400;
    font-size: 14px;
    border-bottom: 1.5px dashed #000;
    color: #050f19;
  }
  &__orders {
  }
  &__availability {
    margin-top: 20px;
    position: relative;
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    color: #050f19;
    &::before {
      content: "";
      background: url("../assets/sber.svg") 0 0 / cover no-repeat;
      width: 20px;
      height: 20px;
      position: absolute;
      left: -30px;
      top: -2px;
      background-size: cover;
    }
  }
  &__offers {
    margin: 19px 0;
    font-weight: 400;
    font-size: 14px;
    color: #1652f0;
  }
}
.parameter {
  margin-bottom: 20px;
  display: flex;
  &__kay {
    font-weight: 400;
    font-size: 14px;
    color: #0a0a0a;
  }
  &__value {
    margin-left: 5px;
    font-weight: 400;
    font-size: 14px;
    color: #708598;
  }
}
.wde {
  margin-top: 20px;
  margin-bottom: 20px;
  display: flex;
}
</style>
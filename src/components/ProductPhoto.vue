<template>
  <div class="product-photo">
    <div class="product-photo__main-photo">
      <img
        src="@/assets/knauf1.png"
        alt=""
        class="product-photo__main-photo__img"
      />
      <button class="product-photo__main-photo__in-list-btn">
        <img
          src="@/assets/plus.svg"
          alt=""
          class="product-photo__main-photo__in-list-btn__img"
        />
        <div class="product-photo__main-photo__in-list-btn__title">
          В список
        </div>
      </button>
      <div class="bestseller">
        <div class="bestseller__title">Хит Продаж</div>
      </div>
      <div class="promotion">
        <div class="promotion__title">Акция</div>
      </div>
      <div class="product-photo__main-photo__zoom">
        Наведите на изображение, чтобы увеличить его
      </div>
    </div>
    <div class="product-photo__navigation">
      <button class="product-photo__navigation__left-btn"></button>
      <div class="product-photo__navigation__more-photos">
        <div class="more-photo">
          <img src="@/assets/knauf3.png" alt="" class="more-photo__img" />
        </div>
        <div class="more-photo">
          <img src="@/assets/knauf3.png" alt="" class="more-photo__img" />
        </div>
        <div class="more-photo active-photo">
          <img src="@/assets/knauf1.png" alt="" class="more-photo__img" />
        </div>
      </div>

      <button class="product-photo__navigation__right-btn"></button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.product-photo {
  &__main-photo {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    width: 350px;
    height: 289px;
    background: #ffffff;
    border: 1px solid #eceff1;
    border-radius: 4px;
    &__in-list-btn {
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      position: absolute;
      width: 93px;
      height: 24px;
      right: 16px;
      top: 16px;
      background: #ffffff;
      /* links */

      border: 1px solid #1652f0;
      border-radius: 2px;
      &__title {
        font-family: "Open Sans", sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 12px;
        color: #1652f0;
      }
    }
    &__zoom {
      position: absolute;
      width: 286px;
      height: 20px;
      top: 253px;
      font-family: "Open Sans", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: 12px;
      line-height: 20px;

      color: #708598;
    }
  }
  &__navigation {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 16px;
    height: 64px;
    width: 350px;
    background-color: rgb(255, 255, 255);

    &__left-btn {
      background-color: #fff;
      background-image: url(@/assets/left.svg);
      background-position: center;
      background-size: 40%;
      background-repeat: no-repeat;
      position: relative;
      height: 24px;
      width: 24px;
    }
    &__right-btn {
      background-color: #fff;
      background-image: url(@/assets/right.svg);
      background-position: center;
      background-size: 40%;
      background-repeat: no-repeat;
      position: relative;
      height: 24px;
      width: 24px;
      height: 24px;
      width: 24px;
    }
    &__more-photos {
      width: 280px;
      display: flex;
      justify-content: space-between;
    }
  }
}
.more-photo {
  height: 64px;
  width: 88px;
  display: flex;
  align-items: center;
  justify-content: center;

  &__img {
    height: 99%;
    overflow: hidden;

    object-fit: cover;
    object-position: bottom;
  }
}

.bestseller {
  top: 16px;
  left: 16px;
  position: absolute;
  background: #f2994a;
  border-radius: 2px;
  height: 24px;
  display: flex;
  padding: 7px 12px;
  &__title {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 10px;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    color: #ffffff;
  }
}

.promotion {
  top: 48px;
  left: 16px;
  position: absolute;
  background: #e92f2f;
  border-radius: 2px;
  height: 24px;
  display: flex;
  padding: 7px 12px;
  &__title {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 10px;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    color: #ffffff;
  }
}
.active-photo {
  background: #ffffff;

  border: 2px solid #1652f0;
  border-radius: 2px;
}
</style>
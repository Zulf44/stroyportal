<template>
  <header class="header">
    <div class="header__hood">
      <button class="location">
        <img src="@/assets/location_img.svg" class="location__img" />
        <div class="location__title">Волгоградская область</div>
      </button>
      <div class="header__hood__menu">
        <button class="header__hood__menu__tenders">Тендеры</button>
        <button class="header__hood__menu__contractors">
          База подрятчиков
        </button>
        <button class="header__hood__menu__services">Другие сервисы</button>
      </div>
    </div>

    <div class="header__main">
      <a href="#" class="logo"> </a>
      <button class="catalog">
        <div class="catalog__img"></div>
        <div class="catalog__title">Каталог</div>
      </button>
      <div class="serch">
        <input
          @focus="autocompleteVisibility = true"
          class="serch__input"
          type="text"
          v-model="query"
          placeholder="Напиши Це...."
        />
        <div
          v-show="
            query.length >= 1 &&
            computedList.length >= 1 &&
            autocompleteVisibility
          "
          class="serch__autocomplete"
        >
          <div
            class="serch__autocomplete__item"
            v-for="item in computedList"
            :key="item.name"
            @click="select(item.name)"
          >
            {{ item.name }}
          </div>
        </div>
        <button class="serch__btn">
          <img src="@/assets/search.svg" alt="" />
        </button>
      </div>

      <div class="list">
        <div class="list__img"></div>
        <div class="list__title">Список</div>
      </div>
      <div class="user-logo"></div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      query: "",
      list: [
        { name: "Цемент красный марка 300" },
        { name: "Цемент хороший" },
        { name: "Цемент не очень хороший" },
        { name: "Штукатурка цементная цокольная Knauf Sockelpultz 25 кг" },
        { name: "Бетоносмеситель Denzel B-200" },
      ],
      autocompleteVisibility: false,
    };
  },
  methods: {
    select(item) {
      this.query = item;
      this.autocompleteVisibility = false;
    },
  },
  computed: {
    computedList() {
      return this.list.filter((item) => {
        return item.name.toLowerCase().indexOf(this.query.toLowerCase()) !== -1;
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  display: block;
  min-height: 32px;

  &__main {
    display: flex;
    align-items: center;
    border-top: 1px solid #eceff1;
    border-bottom: 1px solid #eceff1;
    height: 76px;
    width: 100%;
    background: #ffffff;
    box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.03);
  }
  &__hood {
    font-family: "Open Sans", sans-serif;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 32px;
    background-color: #fff;
    &__menu {
      margin-right: 85px;
      width: 322px;
      display: flex;
      justify-content: space-between;
      font-size: 12px;
      color: #708598;
      &__tenders {
        font-size: 12px;
        color: #708598;
        background-color: #fff;
      }
      &__contractors {
        font-size: 12px;
        color: #708598;
        background-color: #fff;
      }
      &__services {
        font-size: 12px;
        position: relative;
        color: #708598;
        background-color: #fff;
        &::after {
          content: "";
          position: absolute;

          right: -18px;
          background: url("../assets/arrow_down.svg") 0 0 / cover no-repeat;
          width: 18px;
          height: 18px;

          background-size: cover;
          fill: #a48686;
        }
      }
    }
  }
}

.location {
  border: none;
  outline: none;
  background-color: #fff;
  display: flex;
  align-items: center;
  height: 20px;
  margin: 6px 0;
  margin-left: 87px;
  &__img {
    display: block;
    height: 14px;
    margin-right: 8px;
  }
  &__title {
    font-family: "Open Sans", sans-serif;
    font-weight: 400;
    font-size: 12px;
    display: flex;
    justify-content: start;
    align-items: center;
    color: #708598;
  }
}

.logo {
  background: url("../assets/logo.png") 0 0 / cover no-repeat;
  width: 221px;
  height: 48px;
  margin-left: 85px;
}
.catalog {
  display: flex;
  align-items: center;
  justify-content: space-evenly;

  margin-left: 24px;
  width: 116px;
  height: 40px;
  background: #fed83d;
  border-radius: 4px;
  &__title {
    font-family: "Open Sans", sans-serif;
    font-weight: 600;
    font-size: 14px;
    color: #050f19;
  }
  &__img {
    display: block;
    height: 12px;
    width: 18px;
    background: url("../assets/catalog_icon.svg") 0 0 / auto 100% no-repeat;
  }
}

.serch {
  display: flex;
  align-items: center;
  position: relative;
  margin-left: 24px;
  width: 248px;
  height: 40px;
  background: #ffffff;
  border: 1px solid #eceff1;
  border-radius: 4px;
  &__input {
    height: 100%;
    width: 70%;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    color: #708598;
    padding-left: 10px;
  }
  &__autocomplete {
    top: 38px;
    padding: 10px;
    list-style-type: none;
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    color: #000000;
    z-index: 2;
    width: 100%;
    background-color: rgb(255, 255, 255);
    position: absolute;
    border: 1px solid #eceff1;
    &__item {
      display: flex;
      align-items: center;
      justify-content: start;
      border-top: 1px solid #eceff1;

      background-color: #fff;
      min-height: 40px;
      width: 100%;
      font-family: "Open Sans", sans-serif;
      cursor: pointer;
      font-weight: 400;
      font-size: 16px;
      &:hover {
        background-color: rgba(186, 186, 186, 0.281);
      }
    }
  }
  &__btn {
    background-color: #fff;
    height: 20px;
    width: 20px;
    margin-left: 40px;
  }
}

.list {
  margin-left: 302px;
  width: 111px;
  height: 40px;
  background: #fafbfc;
  border: 1px solid #eceff1;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  &__title {
    font-family: "Open Sans", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
  }
  &__img {
    display: block;
    height: 20px;
    width: 16px;
    background: url("../assets/list_icon.svg") 0 0 / auto 100% no-repeat;
  }
}
.user-logo {
  margin-left: 24px;
  width: 40px;
  height: 40px;
  background-color: rgb(79, 47, 220);
  border-radius: 90px;
}
</style>
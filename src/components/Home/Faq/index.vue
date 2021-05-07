<template>
  <div class="faq">
    <div class="faq__content">
      <div class="faq__content__title">
        <h2>Perguntas Frequentes</h2>
      </div>
      <div class="faq__content__list">
        <div
          v-for="(item, index) in itens"
          :key="index"
          class="item"
          type="button"
          @click="setCollapse(item.setCollapse, index)"
        >
          <h2>
            {{ item.title }}
            <span>{{ !item.setCollapse ? "+" : "-" }}</span>
          </h2>
          <div
            :class="
              `item__content item__content--${
                item.collapse ? 'enabled' : 'disabled'
              }`
            "
          >
            <p>
              {{ item.description }}
            </p>
          </div>

          <div class="item__line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import faq from "@/uteis/faq";
export default {
  data: () => ({
    itens: [],
  }),
  watch: {
    collap() {
      this.init();
    },
  },
  mounted() {
    this.init();
    console.log(this.itens);
  },

  methods: {
    init() {
      const arr = [];
      faq.map((item) => {
        item.collapse = false;
        arr.push(item);
        return false;
      });
      this.itens = arr;
    },

    setCollapse(collapse, index) {
      const arr = this.itens;
      if (this.closeToOpen) {
        arr.map((item) => {
          item.collapse = false;
          return false;
        });
      }
      arr[index].collapse = !arr[index].collapse;
      if (collapse) arr[index].collapse = false;
      this.itens = [...arr];
    },
  },
};
</script>

<style lang="scss">
.faq {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
  width: 100%;
  &__content {
    padding: 80px 0;
    width: 100%;
    &__title {
      padding-bottom: 30px;

      h2 {
        font-family: Inter;
        font-style: normal;
        font-weight: bold;
        font-size: 32px;
        line-height: 39px;
        color: #ffffff;
      }
    }
    &__list {
      width: 100%;
    }
  }
}
.item {
  width: 100%;
  max-width: 700px;
  cursor: pointer;

  h2 {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 29px;
    color: var(--color-white);
    margin: 32px 0;
    span {
      font-size: 22px;
      line-height: 29px;
      color: var(--color-white);
    }
  }

  &__content {
    padding-bottom: 32px;

    &--disabled {
      transition: height 0.5s ease-out, display 0.5s;
      transition-delay: 50ms;
      height: 0;
      opacity: 0;
      display: none;
    }

    &--enabled {
      transition: all 0.5s ease;
      height: auto;
      opacity: 1;
    }

    p {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      color: var(--color-light-silver);
    }
  }
  &__line {
    width: 100%;
    height: 1px;
    background-color: var(--color-light-silver);
  }
}
</style>

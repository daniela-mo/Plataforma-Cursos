<template>
  <div class="details">
    <div class="details__content">
      <div class="details__title">
        <h2>Conteúdo detalhado do curso</h2>
      </div>
      <div class="details__list">
        <div
          v-for="(item, index) in context"
          :key="index"
          class="item"
          type="button"
          @click="setCollapse(item.collapse, index)"
        >
          <h2>
            {{ item.title }}
            <span>{{ !item.collapse ? "+" : "-" }}</span>
          </h2>
          <div
            :class="
              `item__content item__content--${
                item.collapse ? 'enabled' : 'disabled'
              }`
            "
          >
            <p>{{ item.description }}</p>
          </div>
          <div class="item__line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import cursos from "@/uteis/cursos";

export default {
  data: () => ({
    context: [],
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
      cursos.map((item) => {
        item.collapse = false; // trás os itens já abertos, o collapse aberto
        arr.push(item); // guarda e trás o conteúdo dentro de item
        return false;
      });
      this.itens = arr;
    },

    setCollapse(collapse, index) {
      const arr = this.itens;
      if (this.closeToOpen) {
        arr.map((item) => {
          item.collapse = false; // faz os tópicos abrirem e fecharem
          return false;
        });
      } //else {
      //   this.Open;
      //   arr.map((item) => {
      //     item.collapse = false; // quando um tópico for aberto, o anterior fecha
      //     return true;
      //   });
      // }

      arr[index].collapse = !arr[index].collapse;
      if (collapse) arr[index].collapse = false; /// sem essa parte, o texto não abre
      this.itens = [...arr];
    },
  },
};
</script>

<style lang="scss">
.details {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  width: 100%;
  flex-direction: column;
  &__content {
    padding: 80px 0;
    &__title {
      padding-bottom: 30px;
      h2 {
        font-size: 32px;
        font-family: Inter;
      }
    }
    &__list {
      width: 100%;
    }
  }
}
.item {
  width: 100%;
  max-width: 550px;
  cursor: pointer;

  h2 {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 29px;
    color: var(--color-blecaute);
    margin: 32px 0;
    span {
      font-size: 22px;
      line-height: 29px;
      color: var(--color-blecaute);
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
      display: flex;
      flex-direction: column;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      color: var(--color-blecaute);
    }
  }
  &__line {
    width: 100%;
    height: 1px;
    background-color: var(--color-dark);
  }
}
</style>

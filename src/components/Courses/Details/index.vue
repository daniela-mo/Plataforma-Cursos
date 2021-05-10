<template>
  <div id="details" class="details">
    <div class="course-details__content">
      <div class="course-details__content__title">
        <h2>Conteúdo detalhado do curso</h2>
      </div>
      <div class="course-details__content__list">
        <div
          v-for="(item, index) in details"
          :key="index"
          class="course-details__content__list__item"
          type="button"
          @click="setCollapse(item.collapse, index)"
        >
          <h2>
            {{ item.title }}
            <span>{{ !item.collapse ? "+" : "-" }}</span>
          </h2>
          <div
            :class="
              `course-details__content__list__item__collapse course-details__content__list__item__collapse--${
                item.collapse ? 'enable' : 'disabled'
              }`
            "
          >
            <p>{{ item.appresent }}</p>
          </div>
          <div class="course-details__list__item__collapse__line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import details from "@/uteis/details";
export default {
  data: () => ({
    details: [],
  }), // minha função
  watch: {
    // acompanhar as mudanças dos valores da variável
    collap() {
      this.init();
    },
  },
  mounted() {
    //
    this.init();
    console.log(this.details);
  },
  methods: {
    init() {
      const array = [];
      details.map((item) => {
        //mapeia os dados dento do details.js para trazelos
        item.collapse = false;
        array.push(item);
        return false;
      });
      this.details = array;
    },
    setCollapse(collapse, index) {
      const array = this.details;
      if (this.closeToOpen) {
        array.map((item) => {
          item.collpase = false; //chama o meu array dentro de details.js e carrega os dados fechados no collpase
          return false;
        });
      }
      array[index].collapse = !array[index].collapse;
      if (collapse) array[index].collapse = false; // o collapse fecha e abre, com o true abrirá e não fechará
      this.details = [...array];
    },
  },
};
</script>

<style lang="scss">
.course-details {
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
      p {
        font-family: Inter;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 39px;
        color: #000;
      }
      &__item {
        width: 100%;
        max-width: 550px;
        cursor: pointer;
        h2 {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          font-family: Helvetica;
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

        &__collapse {
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
            font-family: Helvetica;
            font-style: normal;
            font-weight: normal;
            font-size: 16px;
            line-height: 150%;
            color: #000;
          }
        }
        &__line {
          width: 100%;
          height: 1px;
          background-color: var(--color-dark);
        }
      }
    }
  }
}
</style>

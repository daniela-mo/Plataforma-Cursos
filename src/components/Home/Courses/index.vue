<template>
  <div class="available-courses">
    <div class="available-courses__content">
      <div class="available-courses__content__text">
        <div>
          <h2>Cursos em aberto</h2>
        </div>
        <div class="available-courses__content__text__p">
          <p>
            Cursos e conteúdo para você se capacitar em tecnologia e negócios
            digitais.
          </p>
        </div>
      </div>
      <div class="available-courses__content__cards">
        <Cards :courses="cursosMap" />
        <!-- o item acima é um props para comunicação com a index dos cards -->
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "./Cards";
import cursos from "@/utils/cursos";
export default {
  components: {
    Cards,
  },
  asyncData({ params }) {
    console.log(params);
    return {
      id: params.id,
    };
  },
  data: () => ({
    cursosMap: [],
  }),
  beforeMount() {
    //observa a atividade da função antes de ser chamada na tela
    this.fetch();

    console.log(cursos);
  },
  methods: {
    fetch() {
      const cursosMap = cursos; // mapeia o conteúdo dentro do arquivo cursos.js para reinderiza-los nos cards
      this.cursosMap = cursosMap;
    },
  },
};
</script>

<style lang="scss">
.available-courses {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
  width: 100%;
  &__content {
    margin-top: 60px;
    width: 100%;
    &__text {
      width: 360px;
      h2 {
        color: var(--color-white);
        font-family: Inter;
        font-style: bold;
        line-height: 48px;
        font-size: 40px;
      }
      &__p {
        width: 500px;
        p {
          margin-top: 10px;
          color: #bcbcbc;
          font-family: Helvetica, sans-serif;
          font-style: normal;
          line-height: 150%;
          font-size: 24px;
          color: var(--color-light-silver);
        }
      }
    }
    &__cards {
      display: flex;
      margin-top: 50px;
      width: 100%;
      justify-content: space-between;
      align-items: center;
    }
  }

  @media (max-width: 768px) {
    width: 90%;
    &__text {
      width: 680px;
    }
  }
}
</style>

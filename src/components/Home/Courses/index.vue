<template>
  <div class="courses">
    <div class="courses__content">
      <div class="courses__content__text">
        <div>
          <h2>Cursos em aberto</h2>
        </div>
        <div class="courses__content__text__p">
          <p>
            Cursos e conteúdo para você se capacitar em tecnologia e negócios
            digitais.
          </p>
        </div>
      </div>
      <div class="courses__content__cards">
        <Cards />
        <Cards />
        <Cards />
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "./Cards";
export default {
  components: {
    Cards,
  },
};
</script>

<style lang="scss">
.courses {
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
          color: var(--color-white);
          font-family: Inter;
          font-style: normal;
          line-height: 25px;
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
}
</style>

<template>
  <div>
    <div class="container">
      <nav class="courses__nav">
        <div>Edtech > Nossos cursos > Flutter</div>
      </nav>
      <div class="courses">
        <div class="courses__top">
          <div class="courses__top__text">
            <p>Curso de 08/03 a 29/03</p>

            <h2>
              Flutter
            </h2>

            <strong>Crie e valide formulários para validar conversões</strong>

            <p>
              Expanda suas oportunidades e acelere na direção dos seus
              objetivos.
            </p>
            <div>
              <button class="courses__top__button">
                VER CONTEÚDO DO CURSO
              </button>
            </div>
          </div>

          <div class="courses__top__img">
            <img src="@/assets/ilustracao_flutter.svg" />
          </div>
        </div>
      </div>
    </div>
    <div class="micro">
      <div>
        <Topics />
        <Details />
      </div>
      <div>
        <Briefing />
        <Teacher />
      </div>
    </div>
  </div>
</template>

<script>
import Topics from "@/components/Courses/Topics";
import Details from "@/components/Courses/Details";
import Briefing from "@/components/Courses/Briefing";
import Teacher from "@/components/Courses/Teacher";

export default {
  components: {
    Topics,
    Details,
    Briefing,
    Teacher,
  },
};
</script>

<style lang="scss" scoped>
.courses {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  width: 100%;
  &__nav {
    display: flex;
    max-width: 1170px;
    padding: 50px 0;
    margin: 0 auto;
    width: 100%;
    flex-direction: row;
    color: var(--color-white);
    border-bottom: 1px var(--color-gray-50) solid;
  }
  &__top {
    display: flex;
    justify-content: space-between;
    width: 100%;

    &__text {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      width: 40%;

      h2 {
        color: var(--color-white);
        font-family: Inter;
        font-style: normal;
        font-weight: bold;
        font-size: 48px;
        line-height: 58px;
        font-size: 48px;
      }
      p {
        margin-top: 20px;
        color: #bcbcbc;
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 150%;
      }
      strong {
        color: var(--color-white);
        font-family: Inter;
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 39px;
      }
    }
    &__button {
      background: var(--color-button);
      color: var(--color-black);
      font-size: 12px;
      padding: 14px 10px;
      margin-top: 20px;
      border: none;
      border-radius: 5px;
    }
    &__img {
      height: 100%;
      img {
        height: 100%;
      }
    }
  }
}
.micro {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  width: 100%;
  display: flex;
  justify-content: space-between;
}
</style>

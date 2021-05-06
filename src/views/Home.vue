<template>
  <section class="container">
    <div class="home">
      <div class="home__text">
        <h1 class="home__text__h1">
          Aprenda novas habilidades e avance sua carreira
        </h1>

        <p class="home__text__p">
          Expanda suas oportunidades e acelere na direção dos seus objetivos.
        </p>

        <button class="home__text__button">
          CONHEÇA NOSSOS CURSOS
        </button>
      </div>

      <div class="home__img">
        <img src="@/assets/figuras.svg" />
      </div>
    </div>
    <Listen />
    <Courses />
    <Benefits />
    <Depoiments />
    <Faq />
  </section>
</template>

<script>
import Faq from "@/components/Home/Faq";
import Listen from "@/components/Home/Listen";
import Courses from "@/components/Home/Courses";
import Benefits from "@/components/Home/Benefits";
import Depoiments from "@/components/Home/Depoiments";

export default {
  components: {
    Faq,
    Listen,
    Courses,
    Benefits,
    Depoiments,
  },
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  &__text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    &__h1 {
      color: var(--color-white);
      font-weight: 700;
      font-size: 48px;
    }
    &__p {
      color: var(--color-white);
      margin-top: 20px;
    }
    &__button {
      background: var(--color-button);
      color: var(--color-black);
      font-size: 14px;
      padding: 14px 10px;
      margin-top: 20px;
      border: none;
      border-radius: 5px;
    }
  }
  &__img {
    justify-content: space-between;
  }
}
</style>

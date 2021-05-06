<template>
  <section class="container">
    <div class="home">
      <div class="home__text">
        <div class="home__text__h1">
          <h1>
            Aprenda novas habilidades e avance sua carreira
          </h1>
        </div>
        <div class="home__text__p">
          <p>
            Expanda suas oportunidades e acelere na direção dos seus objetivos.
          </p>
        </div>
        <router-link to="/courses" class="home__text__button">
          CONHEÇA NOSSOS CURSOS
        </router-link>
      </div>

      <div class="home__img">
        <img src="@/assets/figuras.png" />
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

<style lang="scss">
.home {
  display: flex;
  justify-content: space-between;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;

  &__text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding-top: 90px;
    &__h1 {
      width: 500px;
      h1 {
        color: var(--color-white);
        font-weight: 700;
        font-size: 48px;
      }
    }
    &__p {
      width: 450px;
      margin-top: 25px;
      p {
        color: var(--color-white);
        font-family: Inter;
        font-size: 24px;
      }
    }
    &__button {
      background: var(--color-button);
      color: var(--color-black);
      font-size: 14px;
      padding: 14px 10px;
      margin-top: 20px;
      border: none;
      border-radius: 5px;
      text-decoration: none;
    }
  }
  &__img {
    width: 582px;
    height: 495px;
    img {
      width: 582px;
      height: 495px;
    }
  }
}
</style>

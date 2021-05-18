<template>
  <section class="container">
    <div class="home-top">
      <div class="home-top__content">
        <div class="home-top__content__h1">
          <h1>
            Aprenda novas habilidades e avance sua carreira
          </h1>
        </div>
        <div class="home-top__content__p">
          <p>
            Expanda suas oportunidades e acelere na direção dos seus objetivos.
          </p>
        </div>
        <a href="#courses" class="home-top__content__button">
          CONHEÇA NOSSOS CURSOS
        </a>
      </div>

      <div class="home-top__img">
        <img src="@/assets/figuras.png" alt="Mulher estudando" />
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
.container {
  .home-top {
    display: flex;
    justify-content: space-between;
    max-width: 1170px;
    padding: 90px 0;
    margin: 0 auto;
    width: 100%;
    &__content {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding-top: 90px;
      &__h1 {
        width: 500px;
        h1 {
          font-family: Inter;
          font-style: normal;
          color: var(--color-white);
          font-weight: bold;
          font-size: 48px;
        }
      }
      &__p {
        width: 450px;
        margin-top: 25px;
        p {
          color: var(--color-white);
          font-family: Helvetica, sans-serif;
          font-size: 24px;
          line-height: 150%;
        }
      }
      &__button {
        background: var(--color-button);
        color: var(--color-black);
        font-size: 14px;
        font-style: normal;
        font-family: Inter;
        font-weight: 600;
        padding: 14px 10px;
        margin-top: 20px;
        border: none;
        border-radius: 5px;
        text-decoration: none;
        line-height: 17px;
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

  @media (max-width: 768px) {
    width: 100%;
    .home-top {
      flex-direction: column;
      width: 90%;
      height: 600px;
      &__img {
        display: none;
      }
      &__content {
        &__h1 {
          width: 480px;
        }
        &__p {
          width: 480px;
        }
        &__button {
          font-size: 15px;
          padding: 17px 12px;
        }
      }
    }
  }
}
</style>

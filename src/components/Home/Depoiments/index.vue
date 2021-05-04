<template>
  <div class="depoiments">
    <div class="depoiments__content">
      <div class="depoiments__content__text">
        <h2>Depoimentos</h2>
        <p>Velit officia consequat duis enim velit mollit.</p>
      </div>
      <div class="depoiments__content__carousel">
        <Carousel />
        <Carousel />
        <Carousel />
      </div>
    </div>
  </div>
</template>

<script>
import Carousel from "./Carousel";
export default {
  components: {
    Carousel,
  },
};
</script>

<style lang="scss">
.depoiments {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
  width: 100%;
  &__content {
    margin-top: 20px;
    width: 100%;
    &__text {
      width: 320px;

      h2 {
        color: var(--color-white);
        font-family: Inter;
        font-style: bold;
        line-height: 48px;
        font-size: 35px;
      }

      p {
        margin-top: 10px;
        color: var(--color-white);
        font-family: Inter;
        font-style: normal;
        line-height: 25px;
        font-size: 16px;
        color: var(--color-light-silver);
      }
    }
    &__carousel {
      display: flex;
      margin-top: 50px;
      width: 100%;
      justify-content: space-between;
      align-items: center;
    }
  }
}
</style>

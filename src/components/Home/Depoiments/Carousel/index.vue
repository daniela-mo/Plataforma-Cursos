<template>
  <div class="carousel">
    <div class="carousel__content">
      <div>
        <img src="@/assets/Valeria.svg" />
      </div>

      <div class="carousel__content__name">
        <h3>Valéria Hevia</h3>
      </div>

      <div class="carousel__content__text">
        <p>
          Exercitation veniam consequat sunt nostrud amet.Velit officia
          consequat duis enim velit. Exercitation veniam consequat sunt nostrud
        </p>
      </div>
      <div class="carousel__content__text">
        <span>UX/UI Designer</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.carousel {
  width: 384px;
  height: 306px;
  background: #212125;
  border-radius: 8px;
  &__content {
    margin: 30px;
    &__name {
      margin-top: 10px;
      h3 {
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 150%;
        color: #ffffff;
      }
    }
    &__text {
      margin-top: 30px;
      p {
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 150%;
        color: #bcbcbc;
      }
      span {
        width: 154px;
        height: 49px;
        font-weight: 600;
        font-size: 14px;
        color: #fcc419;
      }
    }
  }
}
</style>

<template>
  <div class="faq">
    <div class="faq__content">
      <div class="faq__content__title">
        <h2>Perguntas Frequentes</h2>
      </div>
      <div>
        <img src="@/assets/faq.png" />
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.faq {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
  width: 100%;
  &__content {
    padding: 80px 0;
    &__title {
      padding-bottom: 30px;

      h2 {
        font-family: Inter;
        font-style: normal;
        font-weight: bold;
        font-size: 32px;
        line-height: 39px;
        color: #ffffff;
      }
    }
  }
}
</style>

<template>
  <div class="card">
    <div class="card__topo">
      <div class="card__topo__title">
        <div class="card__topo__mobile">
          <p>MOBILE</p>
        </div>
        <div class="card__topo__flutter">
          <span>Flutter</span>
        </div>
      </div>
      <div>
        <img src="@/assets/ilustracao_flutter.svg" />
      </div>
    </div>
    <div>
      <div class="card__content__date">
        <span>08/03 a 29/03</span>
      </div>
      <div class="card__content__description">
        <p>Crie e valide formulários para validar conversões</p>
      </div>
      <div>
        <button class="card__content__button">IR PARA O CURSO</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.card {
  width: 364px;
  height: 540px;
  background: #212125;
  border-radius: 8px;
  &__topo {
    display: flex;
    padding: 30px;
    &__title {
      display: flex;
      justify-content: space-between;
      &__mobile {
        width: 62px;
        height: 30px;
        background: #141313;
        border-radius: 2px;

        p {
          padding: 8px;
          color: var(--color-white);
          font-family: Inter;
          font-style: normal;
          font-weight: normal;
          font-size: 12px;
          line-height: 14px;
        }
      }
      &__flutter {
        display: flex;
        align-items: flex-end;

        span {
          font-family: Inter;
          font-style: normal;
          font-size: 32px;
          line-height: 39px;
          color: #ffffff;
        }
      }
    }
    &__date {
      font-family: Inter;
      font-style: normal;
      font-weight: bold;
      font-size: 24px;
      line-height: 150%;
      color: #ffffff;
    }
    &__description {
      font-family: Inter;
      font-style: normal;
      font-weight: normal;
      font-size: 24px;
      line-height: 150%;
      color: #bcbcbc;
    }
    &__button {
      padding: 10px;
      width: 154px;
      height: 49px;
      font-weight: 600;
      font-size: 14px;
      background: #fcc419;
      border-radius: 8px;
    }
  }
}
</style>

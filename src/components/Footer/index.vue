<template>
  <div class="container">
    <div class="footer-content">
      <div class="footer-content__all">
        <div class="footer-content__all__logo">
          <img src="@/assets/edtech.svg" />
        </div>

        <div class="footer-content__all__contacts">
          <div class="footer-content__all__contacts__redes">
            <div>
              <span>Redes sociais:</span>
            </div>
            <div class="footer-content__all__contacts__redes__icons">
              <img src="@/assets/linkedin.svg" />
              <img src="@/assets/facebook.svg" />
              <img src="@/assets/twitter.svg" />
              <img src="@/assets/instagram.svg" />
            </div>
          </div>

          <div class="footer-content__all__contacts__email">
            <strong>Fale com a gente: </strong>
            <p>contato@edtech.com.br</p>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      © 2021 EDTECH. Todos os direitos reservados.
    </div>
  </div>
</template>

<style lang="scss">
.footer-content {
  display: flex;
  width: 100%;
  max-width: 1170px;
  margin: 0 auto;
  border-top: 1px var(--color-gray-50) solid;
  &__all {
    padding-top: 60px;
    width: 100%;
    &__logo {
      display: flex;
      padding-bottom: 40px;
    }
    &__contacts {
      display: flex;
      justify-content: space-between;
      width: 100%;
      &__redes {
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
        span {
          font-family: Inter;
          font-style: normal;
          font-weight: normal;
          font-size: 16px;
          line-height: 120%;
          color: #bcbcbc;
        }
        &__icons {
          display: flex;
          justify-content: space-between;
          width: 200px;
          margin: 15px 0px;
          align-items: flex-start;
        }
      }
      &__email {
        display: flex;
        flex-direction: column;

        strong {
          font-family: Inter;
          font-style: normal;
          font-weight: normal;
          font-size: 16px;
          line-height: 180%;
          color: #ffffff;
        }
        p {
          font-family: Inter;
          font-style: normal;
          font-weight: normal;
          font-size: 16px;
          line-height: 150%;
          color: #bcbcbc;
        }
      }
    }
  }
  @media (max-width: 768px) {
    width: 90%;
  }
}
.footer-copyright {
  display: flex;
  color: var(--color-light-silver);
  display: flex;
  width: 100%;
  max-width: 1170px;
  margin: 0px auto;
  padding: 70px 0 15px 0;

  @media (max-width: 768px) {
    width: 90%;
  }
}
</style>

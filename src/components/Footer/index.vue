<template>
  <div class="container">
    <div class="footer">
      <div class="footer__logo">
        <img src="@/assets/edtech.svg" />
      </div>

      <div class="footer__icons">
        <div class="footer__icons__redes">
          <span>Redes sociais:</span>
        </div>
        <img src="@/assets/linkedin.svg" />
        <img src="@/assets/facebook.svg" />
        <img src="@/assets/twitter.svg" />
        <img src="@/assets/instagram.svg" />
      </div>

      <div class="contact">
        Fale com a gente: contato@edtech.com.br
      </div>
      <div class="copyright">
        © 2021 EDTECH. Todos os direitos reservados.
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.footer {
  display: flex;
  width: 90%;
  max-width: 1170px;
  margin: 0 auto;
  border-top: 1px solid #cbcbcb;
  &__logo {
    height: 60px;
  }
  &__icons {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 300px;
    flex-direction: column;

    span {
      font-family: Inter;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      color: #bcbcbc;
    }
  }
}
</style>

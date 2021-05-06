<template>
  <div class="topics">
    <div class="topics__title">
      <h2>Faça esse curso de Flutter e:</h2>
    </div>
    <div class="topics__list">
      <ul>
        <li>Aprenda a criar formulários</li>
        <li>Valide informações de campos</li>
        <li>Aplique máscaras para campos como CPF, CEP e celular</li>
        <li>Habilite a autenticação por biometria</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss">
.topics {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  width: 100%;
  flex-direction: column;
  &__title {
    h2 {
      font-size: 32px;
      font-family: Inter;
    }
  }
  &__list {
    padding-top: 20px;
    ul,
    li {
      font-size: 22px;
      line-height: 150%;
    }
    ul {
      margin-left: 20px;
    }
  }
}
</style>

<template>
  <div class="details">
    <div class="details__title">
      <h2>Conteúdo detalhado do curso</h2>
    </div>
    <div class="details__list">
      <ol>
        <li>Criando um formulário</li>
        <p>Apresentação</p>
        <p>Preparando o projeto</p>
        <p>Área do formulário</p>
        <p>Campos de login</p>

        <li>Validação</li>
        <li>Recursos de app</li>
        <li>Formulário em etapas</li>
        <li>Ajustes</li>
        <li>Autenticação com biometria</li>
      </ol>
    </div>
  </div>
</template>

<style lang="scss">
.details {
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
    padding-top: 40px;
    ol,
    li {
      border-bottom: 1px #6968681e solid;
      font-size: 22px;
      line-height: 400%;
      font-family: Inter;
    }
    ol {
      margin-left: 20px;
    }
    p {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      font-family: Inter;
      padding-top: 16px;
    }
  }
}
</style>

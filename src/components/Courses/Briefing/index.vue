<template>
  <div>
    <div class="briefing">
      <div class="briefing__title">
        <p>Resumo do conteúdo</p>
      </div>
      <div class="briefing__class">
        <div class="briefing__class__items">
          <img src="@/assets/clock.svg" alt="Tempo total das aulas em video" />
          <p>16H Aula</p>
        </div>
        <div class="briefing__class__items">
          <img src="@/assets/youtube.svg" alt="Quantidade de video aulas" />
          <p>6 Vídeos</p>
        </div>
        <div class="briefing__class__items">
          <img src="@/assets/book-open.svg" alt="Quantidade de atividades" />
          4 Atividades
        </div>
      </div>
      <div class="briefing__video">
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/cSa-SMVMGsE"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>

      <div class="briefing__text">
        <p>
          Expanda suas oportunidade e acelere na direção dos seus objetivos.
        </p>
      </div>
      <div class="briefing__button">
        <button class="briefing__button__blue">QUERO ME INSCREVER</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.briefing {
  display: flex;
  width: 520px;
  height: 668px;
  flex-direction: column;
  border: 1px solid #cccccc;
  box-sizing: border-box;
  border-radius: 8px;
  &__title {
    display: flex;
    padding: 30px;
    p {
      font-family: Helvetica;
      font-style: normal;
      font-weight: normal;
      font-size: 24px;
      line-height: 150%;
    }
  }
  &__class {
    display: flex;
    justify-content: space-around;
    padding-bottom: 45px;
    &__items {
      display: flex;
      align-items: center;
      font-family: Helvetica;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      img {
        margin-right: 10px;
      }
    }
  }

  &__video {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 519px;
    height: 260px;
  }
  &__text {
    padding: 50px 35px 20px 35px;
    p {
      font-family: Helvetica;
      font-style: normal;
      font-weight: normal;
      font-size: 24px;
      line-height: 150%;
      color: #000000;
    }
  }
  &__button {
    display: flex;
    justify-content: center;

    &__blue {
      width: 456px;
      height: 80px;
      background: #007afe;
      border-radius: 8px;
      font-family: Inter;
      font-size: 16px;
      font-family: Inter;
      font-weight: 600;
      line-height: 150%;
      color: #ffffff;
      border: none;
    }
  }
}
</style>

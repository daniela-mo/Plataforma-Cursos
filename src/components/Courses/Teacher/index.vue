<template>
  <div class="teacher">
    <div class="teacher__top">
      <div class="teacher__title">
        <p>Instrutor</p>
      </div>

      <div class="teacher__center">
        <div>
          <img src="@/assets/instructor.svg" />
        </div>
        <div class="teacher__center__informations">
          <span>Ricardo Ogliari</span>
          <p>Tech Lead Android</p>
          <div class="teacher__center__informations__icons">
            <img src="@/assets/techer-github.svg" />
            <img src="@/assets/teacher-linkedin.svg" />
            <img src="@/assets/teacher-instagram.svg" />
          </div>
        </div>
      </div>
    </div>
    <div class="teacher__skills">
      <p>
        Ricardo é graduado em Análise e Desenvolvimento de Sistemas. Atualmente
        é mestrando na área de sistemas de informação pela UFRJ. Desenvolvedor
        Full Stack apaixonado por criar aplicativos para dispositivos móveis com
        tecnologias como Ionic e Flutter.
      </p>
    </div>
  </div>
</template>

<style lang="scss">
.teacher {
  display: flex;
  width: 520px;
  height: 469px;
  margin-top: 35px;
  flex-direction: column;
  border: 1px solid #cccccc;
  box-sizing: border-box;
  border-radius: 8px;
  &__title {
    display: flex;
    padding: 30px 30px;
    p {
      font-size: 28px;
      font-family: Inter;
    }
  }
  &__center {
    display: flex;
    justify-content: space-around;
    width: 470px;
    img {
      margin-left: 20px;
      width: 164px;
      height: 164px;
    }
    &__informations {
      display: flex;
      flex-direction: column;
      span {
        font-size: 32px;
        line-height: 150%;
        font-family: Helvetica;
      }
      p {
        font-size: 16px;
        font-weight: normal;
      }
      &__icons {
        display: flex;
        justify-content: space-around;
        width: 120px;
        padding-top: 60px;

        img {
          width: 32px;
          height: 32px;
        }
      }
    }
  }
  &__skills {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 500px;
    p {
      margin: 20px 0 15px 30px;
      font-size: 16px;
      line-height: 150%;
    }
  }
}
</style>

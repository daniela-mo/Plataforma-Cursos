<template>
  <div>
    <div class="container">
      <div class="courses-top__nav">
        <p>
          Edtech >
        </p>
        <router-link to="/" class="courses-top__nav__back"
          >Nossos cursos</router-link
        >
        <p>> Flutter</p>
      </div>
      <div class="courses-top__flutter">
        <div class="courses-top__flutter__course">
          <div class="courses-top__flutter__course__text">
            <p>Curso de 08/03 a 29/03</p>

            <h2>
              Flutter
            </h2>

            <strong>Crie e valide formulários para validar conversões</strong>

            <p>
              Expanda suas oportunidades e acelere na direção dos seus
              objetivos.
            </p>
            <div>
              <a href="#details" class="courses-top__flutter__course__button">
                VER CONTEÚDO DO CURSO
              </a>
            </div>
          </div>

          <div class="courses-top__flutter__course_img">
            <img src="@/assets/ilustracao_flutter.svg" />
          </div>
        </div>
      </div>
    </div>
    <div class="micro">
      <div>
        <Topics />
        <Details />
      </div>
      <div>
        <Briefing />
        <Teacher />
      </div>
    </div>
  </div>
</template>

<script>
import Topics from "@/components/Courses/Topics";
import Details from "@/components/Courses/Details";
import Briefing from "@/components/Courses/Briefing";
import Teacher from "@/components/Courses/Teacher";
import details from "@/uteis/details";

export default {
  components: {
    Topics,
    Details,
    Briefing,
    Teacher,
    details,
  },

  asyncData({ params }) {
    console.log(id);
    return {
      id: params.Id,
    };
  },
  data: () => ({
    // arrow function > forma reduzida de declarar a função
    detailsMap: [],
  }),
  beforeMount() {
    this.fetch();
  },
  methods: {
    fetch() {
      const detailsMap = details; // utilizamos o map pra realizar as alterações ou atualização feitas no array.
      //mapeando os dados dentro da details, e trazendo-os para preencher os campos, sempre atualizando conforme cada alteração feita
      this.detailsMap = detailsMap;
    },
  },
};
</script>

<style lang="scss">
.courses-top__nav {
  display: flex;
  max-width: 1170px;
  padding: 40px 0;
  margin: 0 auto;
  width: 100%;
  flex-direction: row;
  color: var(--color-white);
  border-bottom: 1px var(--color-gray-50) solid;
  p {
    margin-right: 8px;
  }
}
.courses-top__nav__back {
  margin-right: 8px;
  text-decoration: none;
  color: #fff;
}
.courses-top__flutter {
  display: flex;
  max-width: 1170px;
  padding: 60px 0;
  margin: 0 auto;
  width: 100%;

  &__course {
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding-top: 5px;
    &__text {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      width: 40%;

      h2 {
        color: var(--color-white);
        font-family: Inter;
        font-style: normal;
        font-weight: bold;
        font-size: 48px;
        line-height: 58px;
        font-size: 48px;
      }
      p {
        margin-top: 20px;
        color: #bcbcbc;
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 150%;
      }
      strong {
        color: var(--color-white);
        font-family: Inter;
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 39px;
      }
    }
    &__button {
      display: flex;
      align-items: center;
      background: var(--color-button);
      color: var(--color-black);
      font-size: 14px;
      padding: 15px 10px;

      font-weight: 600;
      margin-top: 20px;
      border: none;
      text-decoration: none;
      border-radius: 5px;
    }
    &__img {
      height: 100%;
      img {
        height: 100%;
      }
    }
  }
}
.micro {
  display: flex;
  max-width: 1170px;
  padding: 80px 0;
  margin: 0 auto;
  width: 100%;
  display: flex;
  justify-content: space-between;
}
</style>

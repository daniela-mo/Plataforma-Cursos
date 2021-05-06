<template>
  <div id="courses" class="item-content">
    <div v-for="item in courses" :key="item.id" class="card">
      <div class="card__top">
        <div class="card__top__text">
          <div class="card__top__text__mobile">
            <h3>{{ item.type }}</h3>
          </div>
          <div class="card__top__text__flutter">
            <span>{{ item.name }}</span>
          </div>
        </div>
        <div>
          <img src="@/assets/ilustracao_flutter.svg" />
        </div>
      </div>

      <div class="card__bottom">
        <div class="card__bottom__date">
          <span>{{ item.start }} a {{ item.end }}</span>
        </div>
        <div class="card__bottom__p">
          <p>{{ item.description }}</p>
        </div>
        <div class="card__bottom__button">
          <router-link
            style="text-decoration:none"
            :to="`/courses/${item.useId}`"
            >IR PARA O CURSO</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    courses: Array,
  },
};
</script>

<style lang="scss">
.item-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1170px;
}
.card {
  width: 364px;
  height: 510px;
  background: #212125;
  border-radius: 8px;
  &__top {
    display: flex;
    padding: 20px;
    justify-content: space-between;
    &__text {
      display: flex;
      justify-content: space-between;
      flex-direction: column;
      padding-bottom: 20px;
      &__mobile {
        width: 62px;
        height: 25px;
        background: #141313;
        border-radius: 2px;
        h3 {
          display: flex;
          align-items: center;
          justify-content: center;
          color: var(--color-white);
          width: 62px;
          height: 30px;
          background: #141313;
          border-radius: 2px;
          font-family: Inter;
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
          color: #ffffff;
        }
      }
    }
  }
  &__bottom {
    padding: 0 25px;
    & {
      span {
        font-family: Inter;
        font-style: normal;

        font-size: 20px;
        line-height: 150%;
        color: #ffffff;
      }
    }
    &__p {
      margin-top: 5px;
      p {
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 22px;
        line-height: 150%;
        color: #bcbcbc;
      }
    }
    &__button {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 40px;
      padding: 10px;
      width: 154px;
      height: 49px;
      color: #191820;
      font-weight: 600;
      font-size: 14px;
      background: #fcc419;
      text-decoration: none;
      border-radius: 8px;
      border: none;
    }
  }
}
</style>

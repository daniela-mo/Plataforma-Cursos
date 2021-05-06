<template>
  <div class="item-content">
    <div v-for="item in commit" :key="item.id" class="carousel">
      <div class="carousel__content">
        <div>
          <img :src="item.imageURl" />
        </div>

        <div class="carousel__content__name">
          <h3>{{ item.name }}</h3>
        </div>

        <div class="carousel__content__text">
          <p>{{ item.description }}</p>
        </div>
        <div class="carousel__content__text">
          <span>{{ item.type }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    commit: Array,
  },
};
</script>

<style lang="scss">
.item-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1170px;
  width: 100%;
}

.carousel {
  width: 364px;
  height: 306px;
  background: #212125;
  border-radius: 8px;
  &__content {
    margin: 30px;
    img {
      width: 64px;
      height: 64px;
      border-radius: 50%;
    }
    &__name {
      margin-top: 10px;
      h3 {
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 150%;
        color: #ffffff;
      }
    }
    &__text {
      margin-top: 30px;
      p {
        font-family: Inter;
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 150%;
        color: #bcbcbc;
      }
      span {
        width: 154px;
        height: 49px;
        font-weight: 600;
        font-size: 14px;
        color: #fcc419;
      }
    }
  }
}
</style>

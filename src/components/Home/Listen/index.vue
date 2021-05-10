<template>
  <div class="listen">
    <div class="listen__feather">
      <div class="listen__feather__items">
        <div class="listen__feather__items__img">
          <img src="@/assets/feather_book-open.svg" />
        </div>
        <div class="listen__feather__items__text">
          <span>Amet minim mollit</span>
          <p>
            non deserunt ullamco est sit aliqua dolor do amet sint. Velit
            officia consequat duis enim velit mollit.
          </p>
        </div>
      </div>

      <div class="listen__feather__items">
        <div class="listen__feather__items__img">
          <img src="@/assets/feather_clock.svg" />
        </div>
        <div class="listen__feather__items__text">
          <span>Amet minim mollit</span>
          <p>
            non deserunt ullamco est sit aliqua dolor do amet sint. Velit
            officia consequat duis enim velit mollit.
          </p>
        </div>
      </div>

      <div class="listen__feather__items">
        <div class="listen__feather__items__img">
          <img src="@/assets/feather_award.svg" />
        </div>
        <div class="listen__feather__items__text">
          <span>Amet minim mollit</span>
          <p>
            non deserunt ullamco est sit aliqua dolor do amet sint. Velit
            officia consequat duis enim velit mollit.
          </p>
        </div>
      </div>

      <div class="listen__feather__items">
        <div class="listen__feather__items__img">
          <img src="@/assets/feather_message-square.svg" />
        </div>
        <div class="listen__feather__items__text">
          <span>Amet minim mollit</span>
          <p>
            non deserunt ullamco est sit aliqua dolor do amet sint. Velit
            officia consequat duis enim velit mollit.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.listen {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
  &__feather {
    display: flex;
    flex-wrap: wrap;
    &__items {
      display: flex;
      justify-content: space-between;
      width: 400px;
      margin: 0 104px 40px 0;
      flex-direction: row;
      align-items: flex-start;
      &__img {
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--color-background);
        border-radius: 50%;
        width: 48px;
        height: 48px;

        img {
          width: 24px;
          height: 24px;
        }
      }
      &__text {
        width: 320px;

        span {
          font-family: Inter;
          font-style: normal;
          font-weight: bold;
          font-size: 16px;
          line-height: 150%;
          color: #ffffff;
        }
        p {
          font-family: Inter;
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 150%;
          color: var(--color-light-silver);
        }
      }
    }
  }
}
</style>

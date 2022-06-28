<template>
  <div class="card">
    <div class="dot">
      <img src="../assets/icon-star.svg" alt="">
    </div>
    <h1 class="card__title">
      How did we do?
    </h1>
    <p class="card__description">
      Please let us know how we did with your support request. All feedback is appreciated to help us improve our
      offering!
    </p>
    <form>
      <div class="card__rating">
        <RadioInput v-for="n in 5" :n="n" :key="n">
        </RadioInput>
      </div>
      <button type="submit" class="button">
        Submit
      </button>
    </form>
  </div>
</template>

<script setup>
import RadioInput from './RadioInput.vue';
</script>

<style lang="scss">
.card {
  background-color: darken($color: $color-neutral-Dark-Blue, $amount: 5);
  height: 415px;
  width: 410px;
  border-radius: 25px;
  padding: 32px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  &__title {
    color: $color-neutral-White;
    font-size: 2em;
    font-weight: 700;
  }

  &__rating {
    display: flex;
    justify-content: space-between;
  }
}

.dot {
  background-color: $color-neutral-Dark-Blue;
  height: 50px;
  width: 50px;
  border-radius: 25px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.button {
  background-color: $color-primary-Orange;
  color: $color-neutral-White;
  font-family: $font-family-default;
  font-size: 1em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 2px;
  height: 50px;
  width: 100%;
  border-radius: 25px;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.2s ease-in-out;

  &:hover {
    background-color: $color-neutral-White;
    color: $color-primary-Orange;
  }
}
</style>
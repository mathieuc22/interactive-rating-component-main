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
    <ul class="card__rating">
      <li class="dot dot--selector">1</li>
      <li class="dot dot--selector">2</li>
      <li class="dot dot--selector">3</li>
      <li class="dot dot--selector">4</li>
      <li class="dot dot--selector">5</li>
    </ul>
    <button class="button">
      Submit
    </button>
  </div>
</template>

<style lang="scss" scoped>
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

  &--selector {
    cursor: pointer;
    font-weight: 700;
    transition: all 0.2s ease-in-out;

    &:hover {
      background-color: $color-primary-Orange;
      color: $color-neutral-White;
    }
  }
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
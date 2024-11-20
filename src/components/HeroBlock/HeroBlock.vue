<template>
  <div class="hero">
    <div class="hero__info">
      <h1 class="hero__info-title">AWESOME HTML5 GAMES - NO MONEY!</h1>
      <h2 class="hero__info-subtitle">Your Perfect Place To Get Some Fun And Excitement</h2>
      <div class="hero__buttons">
        <button class="hero__button hero__button-border">Log In</button>
        <button class="hero__button">Play</button>
      </div>
    </div>
    <div class="form">
      <div class="form__text">
        <h3 class="form__title">Create a free account now</h3>
        <div class="form__icons">
          <div class="form__icon">
            <img src="../../assets/images/icons/dice.png" alt="" />
            <span>1000+ Games available</span>
          </div>
          <div class="form__icon">
            <img src="../../assets/images/icons/slot.png" alt="" />
            <span>New game Every week</span>
          </div>
          <div class="form__icon">
            <img src="../../assets/images/icons/24h.png" alt="" />
            <span>Support our users 24/7</span>
          </div>
        </div>
      </div>
      <div class="form__wrapper">
        <form action="">
          <div class="form__inputs">
            <input type="text" class="form__input" placeholder="Firstname" required />
            <input type="text" class="form__input" placeholder="Lastname" required />
            <input type="email" class="form__input" placeholder="Email Address" required />
            <button class="form__button" type="submit">Join Now</button>
          </div>
          <div class="form__policy">
            <input type="checkbox" name="" id="form__policy" />
            <label for="form__policy">I Accept The <a href="#">Privacy Policy</a></label>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss" src="./HeroBlock.scss"></style>

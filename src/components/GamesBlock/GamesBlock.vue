<script setup>
import GameBlock from '../GameBlock/GameBlock.vue';
</script>
<template>
  <div class="games">
    <div class="games__title">
      <h2>Our Games</h2>
      <div class="games__subtitle">
        <p>Get Virtual Welcome bonus after Sign Up</p>
        <a href="">All games</a>
      </div>
    </div>
    <div class="games__catalog">
      <div class="games__items">
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.2813.jpg"
          title="Double Jackpot"
          text="NetentGames"
        />
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.4298.jpg"
          title="All Aboard: Dynamic corp"
          text="RushGameStudio"
        />
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.4749.jpg"
          title="Book Of Tombs"
          text="NetentGames"
        />
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.4779.jpg"
          title="Rudolph’s Ride"
          text="NetentGames"
        />
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.5423.jpg"
          title="Starburst XXXtreme"
          text="StarBurst Inc."
        />
        <GameBlock
          imageUrl="../src/assets/images/games/gametype.1882.jpg"
          title="Black Diamond"
          text="RushGameStudio"
        />
      </div>
      <div class="games__banners">
        <div class="games__banners-top">
          <div class="games__banner">
            <img
              src="@/assets/images/games/DynamiteRichesMW_BigWin_385x190.jpeg"
              alt="games_banner"
            />
            <div class="games__banner-text">
              <h3>Dynamite Riches Megaways</h3>
              <p>
                Miners revealed a gain of €46,672 for Sandra M.! You too, dynamite the reels of the
                Red Tiger Daily Jackpot machines
              </p>
            </div>
            <a href="" class="games__banner-link">Play now</a>
          </div>
          <div class="games__banner">
            <img src="@/assets/images/games/GOTM_GatorGold_385x190.jpeg" alt="games_banner" />
            <div class="games__banner-text">
              <h3>Gator Gold Deluxe Gigablox</h3>
              <p>
                These swamps conceal many dangers but especially precious treasures. Will you be
                able to find them?
              </p>
            </div>
            <a href="" class="games__banner-link">Play now</a>
          </div>
        </div>
        <div class="games__banners-bottom">
          <div class="games__banner">
            <img src="@/assets/images/banner_promo.jpeg" alt="games_banner" />
            <div class="games__banner-text">
              <h3>Our deals are not to be missed</h3>
              <p>Discover a wide range of weekly promotions</p>
            </div>
            <a href="" class="games__banner-link">Read more</a>
          </div>
        </div>
      </div>
    </div>
    <p class="games__warm">
      * We don't offer opportunities to play for real money. Our games are free demo. All games were
      invented for entertainment purposes only and do not offer real money prizes.
    </p>
  </div>
</template>
<style lang="css" scoped src="./GamesBlock.scss"></style>

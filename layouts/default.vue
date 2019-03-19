<template>
  <div class="app">
    <header class="header">
      <nuxt-link class="header__link header__link--name" to="/">Martin Rojo</nuxt-link>
      <a class="header__link header__link--email" href="mailto:wat.martinrojo@gmail.com">email</a>
      <a class="header__link header__link--twitter" href="https://twitter.com/martinrojo__" target="__blank">twitter</a>
      <a class="header__link header__link--instagram" href="https://www.instagram.com/shmvrts/" target="__blank">instagram</a>
    </header>
    <nuxt class="view"/>
    <a class="email-button" href="mailto:wat.martinrojo@gmail.com">email me</a>
  </div>
</template>

<style lang="scss">
.app {
  max-width: 1000px;
  margin: 0 auto;
  padding-bottom: 200px;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';
  @media only screen and (max-width: 1200px) {
    padding: 0 100px 150px;
    max-width: 100%;
  }
  @media only screen and (max-width: 880px) {
    padding: 0 50px 100px;
  }
  @media only screen and (max-width: 600px) {
    padding: 0 30px 60px;
  }
  @media only screen and (max-width: 480px) {
    padding: 0 20px 50px;
  }
}

.header {
  display: flex;
  align-items: center;
  margin-top: 40px;
  flex-wrap: wrap;
  &__link {
    font-size: 14px;
    font-weight: 700;
    color: #000;
    margin-right: 20px;
    &--{
      &name {
        text-transform: uppercase;
        font-size: 16px;
        margin-right: 40px;
        @media only screen and (max-width: 440px) {
          width: 100%;
          margin: 0 0 10px 0;
        }
      }
      &email {

      }
      &twitter {
        color: #1ca1f2;
      }
      &instagram {
        background: #fec66c; /* Old browsers */
        background: -moz-linear-gradient(45deg, #fec66c 0%, #f77638 25%, #e33e5f 50%, #bc318f 75%, #6558ca 100%); /* FF3.6-15 */
        background: -webkit-linear-gradient(45deg, #fec66c 0%,#f77638 25%,#e33e5f 50%,#bc318f 75%,#6558ca 100%); /* Chrome10-25,Safari5.1-6 */
        background: linear-gradient(45deg, #fec66c 0%,#f77638 25%,#e33e5f 50%,#bc318f 75%,#6558ca 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
      }
    }
  }
}

.view {
  margin-top: 80px;
  @media only screen and (max-width: 600px) {
    margin-top: 40px;
  }
}

.email-button {
  color: #d43030;
  font-size: 32px;
  font-weight: 700;
  position: fixed;
  bottom: 30px;
  right: 40px;
  @media only screen and (max-width: 760px) {
    display: none;
  }
}

</style>

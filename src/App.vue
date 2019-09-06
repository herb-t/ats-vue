<style>
  body,
  html {
    height: 100%;
    width: 100%;
  }

  body {
    background: #fff;
    color: #202124;
    cursor: auto;
    font-family: 'Lato', Arial, Helvetica, sans-serif;
    font-size: 1em;
    font-style: normal;
    font-weight: 300;
    line-height: 1.444;
    margin: 0;
    overflow-x: hidden;
    padding: 0;
    position: relative;
    overflow-wrap: break-word;
    word-wrap: break-word;
  }

  p, h1, h2, h3,
  h4, span, a {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    color: #cf6059;
  }

  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  p,
  a,
  span {
    line-height: 1.71429;
    font-size: 14px;
    font-weight: 300;
    letter-spacing: .25px;
  }

  h1,
  h2 {
    font-family: 'Nixie One',cursive;
    font-size: 56px;
    font-weight: 100;
  }

  h1 {
    font-size: 32px;
    font-weight: 400;
    letter-spacing: 0;
    line-height: 38px;
  }

  h2 {
    font-size: 28px;
    font-weight: 500;
    line-height: 1.25;
  }

  h3 {
    font-size: 20px;
    font-weight: 300;
    letter-spacing: 0;
    line-height: 28px;
  }

  h4 {
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 0;
    line-height: 24px;
  }

  .ats-page {
    box-sizing: content-box;
    margin: 0 auto;
    max-width: 568px;
    padding: 0 16px;
    width: auto;
  }

  .ats-button {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    background-color: #cf6059;
    border: none;
    border-radius: 4px;
    box-sizing: border-box;
    color: #fff;
    cursor: pointer;
    display: inline-block;
    font-family: 'Lato', Arial, Helvetica, sans-serif;
    font-size: 14px;
    font-weight: 500;
    height: auto;
    line-height: 1;
    letter-spacing: .75px;
    margin: 8px 0;
    padding: 15px 24px;
    transition: color .15s linear, background-color .15s linear;
    vertical-align: middle;
  }

  .ats-button:hover {
    background-color: #b6534c;
    border: 0;
    outline: 0;
  }

  .ats-button:focus {
    border: 0;
    outline: 0;
  }

  .ats-grid {
    align-items: center;
    box-sizing: border-box;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 -2.65152%;
  }

  .ats-grid__col {
    flex: auto 0 auto;
    margin: 0 2.65152%;
    width: 100%;
  }

  .modal-is-showing {
    display: block !important;
  }

  .ats-card__span {
    font-weight: 700 !important;
  }

  body.modal-is-showing,
  body.header__drawer--is-showing {
    overflow: hidden;
  }

  @media (min-width: 600px) {
    h1 {
      font-size: 38px;
      line-height: 44px;
    }

    h2 {
      font-size: 32px;
      line-height: 40px;
    }

    h3 {
      font-size: 24px;
      line-height: 32px;
    }

    .ats-page {
      max-width: 960px;
      padding: 0 32px;
    }
  }

  @media (min-width: 900px) {
    .ats-button {
      font-size: 16px;
      letter-spacing: .5px;
      padding: 17px 24px;
    }

    .ats-grid__col--2 {
      flex-basis: 47.92401%;
      margin: 0 1.03799%;
      width: 47.92401%;
    }

    .ats-grid__col--3 {
      flex-basis: 31.25734%;
      margin: 0 1.03799%;
      width: 31.25734%;
    }
  }

  @media (min-width: 1024px) {
    p,
    a,
    span {
      line-height: 1.625;
      font-size: 16px;
      letter-spacing: 0;
    }

    h1 {
      font-size: 52px;
      letter-spacing: -.25px;
      line-height: 60px;
    }

    h2 {
      font-size: 36px;
      letter-spacing: -.25px;
      line-height: 44px;
    }

    h3 {
      font-size: 28px;
      line-height: 36px;
    }

    h4 {
      font-size: 18px;
      line-height: 30px;
    }
  }

</style>

<template>
  <div id="ats">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

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
  }

  p,
  span {
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 0.25px;
  }

  h1,
  h2 {
    font-family: 'Nixie One',cursive;
    font-size: 56px;
    font-weight: 100;
  }

  h2 {
    font-size: 32px;
  }

  .ats-page {
    box-sizing: border-box;
    margin: 0 auto;
    max-width: 1280px;
    padding: 0 32px;
  }

  .ats-button {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    background-color: #cf6059;
    border: none;
    border-radius: 4px;
    color: #fff;
    cursor: pointer;
    display: inline-block;
    font-family: 'Lato', Arial, Helvetica, sans-serif;
    font-size: 16px;
    font-weight: 500;
    height: auto;
    line-height: 1;
    letter-spacing: .5px;
    margin: 8px 0;
    padding: 17px 24px;
    transition: color .15s linear, background-color .15s linear;
    vertical-align: middle;
  }

  .ats-button:hover {
    background-color: #b6534c;
    outline: 0;
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

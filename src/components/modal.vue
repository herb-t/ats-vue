<style scoped>
  .modal {
    display: none;
    opacity: 0;
    position: fixed;
    z-index: 175;
  }

  .modal__container {
    display: block;
    background: #fff;
    box-shadow: 0 14px 28px rgba(0,0,0,.25), 0 10px 10px rgba(0,0,0,.22);
    border-radius: 4px;
    height: 93%;
    left: 50%;
    max-width: 700px;
    overflow: auto;
    padding: 16px;
    position: fixed;
    top: 50%;
    transform: translate(-50%, -45%);
    width: 90%;
    z-index: 180;
  }

  .modal__content {
    height: 100%;
  }

  .modal__backdrop {
    background: rgba(0,0,0,0.4);
    bottom: 0;
    left: 0;
    opacity: 0;
    position: fixed;
    right: 0;
    top: 0;
    z-index: 175;
  }

  .modal__close {
    position: absolute;
    right: 16px;
    top: 16px;
    z-index: 185;
  }

  .modal__close-btn {
    background: transparent;
    border: 0;
    cursor: pointer;
    outline: 0;
  }

  .modal__close-btn svg {
    fill: #cf6059;
    height: 32px;
    width: 32px;
  }

  .modal__iframe {
    height: 100%;
    width: 100%;
  }

  @media (min-width: 600px) {
    .modal__container {
      height: 70%;
      padding: 32px;
      top: 54%;
      width: 70%;
    }
  }

  @media (min-width: 900px) {
    /* .modal__container {
      height: 70%;
      padding: 32px;
      width: 70%;
    } */

    .modal__backdrop {
      top: 64px;
    }
  }
</style>

<template>
  <div class="modal">
    <div class="modal__container">
      <div class="modal__close">
        <button class="modal__close-btn modal-toggle">
            <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
            viewBox="0 0 51.976 51.976" style="enable-background:new 0 0 51.976 51.976;" xml:space="preserve">
           <g>
             <path d="M44.373,7.603c-10.137-10.137-26.632-10.138-36.77,0c-10.138,10.138-10.137,26.632,0,36.77s26.632,10.138,36.77,0
               C54.51,34.235,54.51,17.74,44.373,7.603z M36.241,36.241c-0.781,0.781-2.047,0.781-2.828,0l-7.425-7.425l-7.778,7.778
               c-0.781,0.781-2.047,0.781-2.828,0c-0.781-0.781-0.781-2.047,0-2.828l7.778-7.778l-7.425-7.425c-0.781-0.781-0.781-2.048,0-2.828
               c0.781-0.781,2.047-0.781,2.828,0l7.425,7.425l7.071-7.071c0.781-0.781,2.047-0.781,2.828,0c0.781,0.781,0.781,2.047,0,2.828
               l-7.071,7.071l7.425,7.425C37.022,34.194,37.022,35.46,36.241,36.241z"/>
           </g>
         </svg>
        </button>
      </div>
      <div class="modal__content">
          <iframe class="modal__iframe" src="https://docs.google.com/forms/d/e/1FAIpQLSeLiZBTBSEXeWDxZsS411gzx4ELKVnVaXF5b9Q9_INGg_Pkpg/viewform?embedded=true" width="640" height="1108" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
      </div>
    </div>

    <div class="modal__backdrop modal-toggle"></div>
  </div>
</template>

<script>
export default {
  name: 'modal',
  data () {
    return {
      label: 'Modal'
    }
  }
}
</script>

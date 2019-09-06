<style scoped>
  .share {
    position: fixed;
    right: 8px;
    top: 72px;
    transform: translateX(200px);
    z-index: 200;
  }

  .share__list-item {
    border-radius: 50%;
    box-shadow: 0 0.27778rem 0.27778rem 0 rgba(0,0,0,.2);
    background: #fff;
    display: block;
    margin-bottom: 12px;
  }

  .share__list-link {
    background: #fff;
    padding: 0;
    text-align: center;
  }

  .share__icon {
    display: block;
    fill: #ce6058;
    height: 32px;
    width: 32px;
  }

</style>

<template>
  <div class="share">
    <div class="share__content">
      <ul class="share__list">
        <li class="share__list-item">
          <a href="#" class="share__list-link">
            <!-- facebook -->
            <svg version="1.1" class="share__icon" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
            viewBox="0 0 38.4 38.4" style="enable-background:new 0 0 38.4 38.4;" xml:space="preserve">
              <path id="facebook-circle-icon_2_" class="st0" d="M19.2,0C8.6,0,0,8.6,0,19.2c0,10.6,8.6,19.2,19.2,19.2s19.2-8.6,19.2-19.2
              S29.8,0,19.2,0z M24.9,11.3c0,0-1.9,0-2.7,0c-0.9,0-1.1,0.4-1.1,1.4c0,0.8,0,2.4,0,2.4h3.8l-0.4,4.2H21v12.4h-5V19.3h-2.6v-4.2h2.7
              c0,0,0-0.6,0-3.3c0-3.1,1.7-4.7,5.4-4.7c0.6,0,3.4,0,3.4,0V11.3L24.9,11.3z"/>
            </svg>
          </a>
        </li>
        <li class="share__list-item">
          <a href="#" class="share__list-link">
            <!-- twitter -->
            <svg version="1.1" class="share__icon" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 38.4 38.4" style="enable-background:new 0 0 38.4 38.4;" xml:space="preserve">
              <path id="twitter-4-icon_2_" class="st0" d="M19.2,0C8.6,0,0,8.6,0,19.2c0,10.6,8.6,19.2,19.2,19.2s19.2-8.6,19.2-19.2
                C38.4,8.6,29.8,0,19.2,0z M28.8,15.9c0.3,6.3-4.4,13.2-12.7,13.2c-2.5,0-4.9-0.7-6.8-2c2.4,0.3,4.7-0.4,6.6-1.8
                c-1.9,0-3.6-1.3-4.2-3.1c0.7,0.1,1.4,0.1,2-0.1c-2.1-0.4-3.6-2.4-3.6-4.4c0.6,0.3,1.3,0.5,2,0.6c-2-1.3-2.5-3.9-1.4-5.9
                c2.2,2.7,5.5,4.5,9.2,4.7c-0.6-2.8,1.5-5.5,4.3-5.5c1.3,0,2.4,0.5,3.3,1.4c1-0.2,2-0.6,2.8-1.1c-0.3,1-1,1.9-2,2.5
                c0.9-0.1,1.8-0.3,2.6-0.7C30.4,14.5,29.7,15.3,28.8,15.9z"/>
            </svg>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'share',
  data () {
    return {
      label: 'Contact'
    }
  }
}
</script>

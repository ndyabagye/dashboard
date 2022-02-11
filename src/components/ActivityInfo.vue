<template>
  <div class="activity-info ps-5">
      <div class="first-info d-flex flex-row pt-3">
          <div class="info-icon">
              <svg xmlns="http://www.w3.org/2000/svg" weight="32" height="32" fill="#255daf" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M466.5 83.71l-192-80C269.6 1.67 261.3 0 256 0C250.7 0 242.5 1.67 237.6 3.702l-192 80C27.7 91.1 16 108.6 16 127.1c0 257.2 189.2 384 239.1 384c51.1 0 240-128.2 240-384C496 108.6 484.3 91.1 466.5 83.71zM256 446.5l.0234-381.1c.0059-.0234 0 0 0 0l175.9 73.17C427.8 319.7 319 417.1 256 446.5z"/></svg>
          </div>
          <div class="info-text ps-3">
              <h4>Insurance</h4>
              <p class="text-muted fs-6">Property coverage</p>
          </div>
      </div>
      <div class="second-info pt-4">
          <h6>LTC Wallet</h6>
          <p class="text-muted">Personal account</p>
      </div>
      <div class="third-info pt-4">
          <h6>7 Jun, 21</h6>
          <p class="text-muted">Last payment</p>
      </div>
      <div class="fourth-info pt-4">
          <h6> -10.24 LTC</h6>
          <p class="text-muted">Balance</p>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.info-icon{
 display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 50px;
  border-radius: 25%;
  background-color: #e7eef8;
}
.activity-info{
    display:grid;
    grid-template-columns: 2fr 1fr 1fr 1fr !important;
}
</style>
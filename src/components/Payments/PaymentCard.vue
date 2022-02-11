<template>
  <div class="card mb-3 me-3">
    <div class="card-top mt-2 mb-3">
      <div class="card-icon">
        <img :src="svg" alt="" />
      </div>
      <div class="card-text d-flex flex-row">
        <h6 class="fs-6">Received {{ title }}</h6>
        <font-awesome-icon icon="fa-solid fa-chevron-down" />
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="16"
          width="16"
          fill="#c0c9d6"
          viewBox="0 0 448 512"
        >
          <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
          <path
            d="M224 416c-8.188 0-16.38-3.125-22.62-9.375l-192-192c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L224 338.8l169.4-169.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-192 192C240.4 412.9 232.2 416 224 416z"
          />
        </svg>
        <!-- icon -->
      </div>
      <div class="card-price">
        <h6 class="fs-6 text-sm text-muted p-1 shadow rounded me-2">{{ btc }}</h6>
      </div>
    </div>
    <div class="card-bottom my-2 ms-5 flex-row align-items-end justify-content-between">
        <div class="date">
            <br>
            <h6 class="fs-6 text-muted">
            {{date}}
            </h6>
        </div>
        <div class="people ms-5">
            <img :src="image" class="img-fluid peopleImage" alt="" />
        </div>
    </div>
  </div>
</template>

<script>
import image from '../../img/profile.svg';

export default {
    props: {
        title: String,
svg: String,
date: String,
btc: String,
},
    data(){
        return{

  image
      }
  }
};
</script>

<style>
.peopleImage{
    height: 60px;
    width: 60px;
}
.card-bottom{
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.card-top {
  display: grid;
  grid-template-columns: 1.2fr 3fr 2fr;
}

.card-price{
    width: 100px;
}
</style>

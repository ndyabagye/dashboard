<template>
  <div class="card p-3" v-bind:style="{ backgroundColor: color }">
    <div class="header d-flex justify-content-between flex-row">
      <h6>{{ title }}</h6>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="#514e86"
        class="bi bi-three-dots-vertical"
        viewBox="0 0 16 16"
      >
        <path
          d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0z"
        />
      </svg>
    </div>
    <div class="body m-2">
        <img :src="svg" alt="">
    </div>
    <div class="currency-info d-flex flex-column">
      <h3>
        {{ btc }}
      </h3>
      <h5>
        {{ usd }}
      </h5>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        title:String,
        color:String,
        btc: String,
        usd:String,
        svg:String,
    },
  data() {
    return {

    };
  },
};
</script>

<style>
h3,h5{
    color:#514e86
}
</style>

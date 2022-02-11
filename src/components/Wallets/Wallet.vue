<template>
  <div class="wallet">
    <div class="wallet-info d-flex flex-row">
      <div class="wallet-icon me-2">
        <img :src="svg" class="img-fluid" alt="" />
      </div>
      <div class="wallet-text">
        <h5>{{ title }}</h5>
        <p class="text-sm" v-bind:style="{color: '#64557f' }">{{ subtitle }}</p>
      </div>
    </div>
    <div class="wallet-price justify-content-end">
      <h5>{{ percent }}</h5>
      <h6 v-bind:style="{ color: textColor }">{{ subpercent }}</h6>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    svg: String,
    title: String,
    subtitle: String,
    percent: String,
    subpercent: String,
    textColor: String,
  },
};
</script>

<style>
.wallet-icon {
  height: 50px !important;
  width: 50px !important;
  border-radius: 25% !important;
}

.wallet {
  display: grid;
  grid-template-columns: 3fr 1fr !important;
}
</style>

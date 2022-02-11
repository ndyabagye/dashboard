<template>
  <div class="activity-info ps-5">
    <div class="first-info d-flex flex-row pt-3">
      <div class="info-icon" v-bind:style="{backgroundColor: color }">
        <img :src="svg" alt="svg" />
      </div>
      <div class="info-text ps-3">
        <h6 class="fs-4">{{ title }}</h6>
        <p class="text-muted fs-6">{{ subtitle }}</p>
      </div>
    </div>
    <div class="second-info pt-4">
      <h6>{{ wallet }}</h6>
      <p class="text-muted">{{ account }}</p>
    </div>
    <div class="third-info pt-4">
      <h6>{{ date }}</h6>
      <p class="text-muted">{{ payment }}</p>
    </div>
    <div class="fourth-info pt-4">
      <h6>{{ balance }}</h6>
      <p class="text-muted">Balance</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    subtitle: String,
    wallet: String,
    account: String,
    date: String,
    payment: String,
    balance: String,
    svg: String,
    color:String,
  },
};
</script>

<style>
.info-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
  width: 60px;
  border-radius: 25%;
  /* background-color: #e7eef8; */
}
.activity-info {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr !important;
}
</style>

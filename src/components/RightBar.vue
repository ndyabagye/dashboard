<template>
  <div class="right-bar ps-5 pt-3">
    <nav class="nav-info align-items-end">
      <div>
        <p class="text-muted">Quit</p>
      </div>
      <div>
        <p class="text-muted">Personal</p>
      </div>
      <div class="profile">
        <img :src="Profile" class="img-fluid" alt="" />
      </div>
    </nav>
    <div class="d-flex flex-row justify-content-around my-3">
      <h6 class="fs-3">Payments</h6>
      <h6 class="fs-6 px-2 py-2 shadow rounded">Clear</h6>
    </div>
    <PaymentCard
      v-for="payment in paymentData"
      :key="payment.id"
      :color="payment.color"
      :title="payment.title"
      :btc="payment.btc"
      :usd="payment.usd"
      :date="payment.date"
      :svg="payment.svg"
    />
    <div class="new-transfer rounded me-3 p-2">
      <div class="plus bg-white">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="#227ffb"
          width="18"
          height="18"
          viewBox="0 0 512 512"
        >
          <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
          <path
            d="M362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32zM421.7 220.3L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3z"
          />
        </svg>
      </div>
      <div
        class="d-flex ms-5 flex-row justify-content-around align-items-center"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="24"
          width="24"
          fill="#6961aa"
          viewBox="0 0 448 512"
        >
          <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
          <path
            d="M432 256c0 17.69-14.33 32.01-32 32.01H256v144c0 17.69-14.33 31.99-32 31.99s-32-14.3-32-31.99v-144H48c-17.67 0-32-14.32-32-32.01s14.33-31.99 32-31.99H192v-144c0-17.69 14.33-32.01 32-32.01s32 14.32 32 32.01v144h144C417.7 224 432 238.3 432 256z"
          />
        </svg>
        <h6 class="fs-6 mt-2 ms-2 new">New Transfer</h6>
      </div>
      <div></div>
    </div>

    <div class="d-flex flex-row my-4">
      <h6 class="fs-3">Wallets</h6>
    </div>
    <Wallet
      v-for="wallet in walletData"
      :key="wallet.id"
      :textColor="wallet.textColor"
      :title="wallet.title"
      :subtitle="wallet.subtitle"
      :percent="wallet.percent"
      :subpercent="wallet.subpercent"
      :svg="wallet.svg"
    />
  </div>
</template>

<script>
import Profile from '../img/profile.png';
import PaymentCard from './Payments/PaymentCard.vue';
import Wallet from './Wallets/Wallet.vue';
import Litecoin from '../svg/litecoin-solid.svg';
import Link from '@/svg/link.svg';
// wallet svg
import BTE from '../img/BTE.png';
import DAI from '../img/DAI.png';
import XRP from '../img/XRP.png';
import USDT from '../img/USDT.png';

export default {
  data() {
    return {
      paymentData: [
        {
          id: 'LiteCoin',
          title: 'LTC',
          date: '09/08/2020 19:22',
          btc: '+ 15.08 USD',
          svg: Litecoin,
          color: '#f6886e',
        },
        {
          id: 'Link',
          title: 'LINK',
          date: '09/08/2020 19:22',
          btc: '+ 957.96 USD',
          svg: Link,
          color: '#3bdfc2',
        },
      ],
      walletData: [
        {
          id: 'BTE',
          title: 'BTE',
          subtitle: 'Bitcoin',
          percent: '37%',
          subpercent: '-2.5%',
          svg: BTE,
          textColor:'#81e5c7',
        },
        {
          id: 'DAI',
          title: 'DAI',
          subtitle: 'Dai',
          percent: '23%',
          subpercent: '+7.2%',
          svg: DAI,
          textColor:"#64557f",
        },
        {
          id: 'XRP',
          title: 'XRP',
          subtitle: 'Ripple',
          percent: '20%',
          subpercent: '-3.1%',
          svg: XRP,
          textColor:'#81e5c7',
        },
        {
          id: 'USDT',
          title: 'USDT',
          subtitle: 'Tether',
          percent: '17%',
          subpercent: '-1.8%',
          svg: USDT,
          textColor:"#64557f",
        },
      ],
      Profile,
    };
  },
  components: {
    Wallet,
    PaymentCard,
  },
};
</script>

<style>
.new {
  color: #6961a9;
  width: 100px;
}

.new-transfer {
  background-color: #d8d7eb;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
.profile {
  height: 50px;
  width: 50px;
}
.nav-info {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr !important;
}
.right-bar {
  background-color: #f9faff;
}
</style>

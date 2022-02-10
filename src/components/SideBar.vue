<template>
  <div class="sidebar ps-5 bg-light">
    <div class="logo">
        <img  :src="Logo" class="img-fluid" alt="logo">
    </div>
    <div class="icon-section-one">
      <div class="col" v-for="icon in iconsListOne" :key="icon.id">
        <img :src="icon.icon" />
        <div class="pt-3 pb-2">
          {{ icon.text }}
        </div>
      </div>
    </div>
    <div><br /><br /><br /></div>
    <div class="icon-section-two">
      <div class="col" v-for="icon in iconsListTwo" :key="icon.id">
        <img :src="icon.icon" />
        <div class="pt-3 pb-2">
          {{ icon.text }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '../img/Logo.png';
import Dashboard from '../img/dashboard.png';
import Calculator from '../img/calculator.png';
import Wallets from '../img/wallet.png';
import Savings from '../img/save-money.png';
import Currencies from '../img/currencies.png';
import Expenses from '../img/expenses.png';
import Upcoming from '../img/fire.png';
import Food from '../img/tea-mug.png';
import Health from '../img/heartbeat.png';
import Account from '../img/user.png';

export default {
  data() {
    return {
      iconsListOne: [
        { id: 'Dashboard', text: 'Dashboard', icon: Dashboard },
        { id: 'Calculator', text: 'Calculator', icon: Calculator },
        { id: 'Wallets', text: 'Wallets', icon: Wallets },
        { id: 'Savings', text: 'Savings', icon: Savings },
        { id: 'Currencies', text: 'Dashboard', icon: Currencies },
        { id: 'Expenses', text: 'Expenses', icon: Expenses },
      ],
      iconsListTwo: [
        { id: 'Upcoming', text: 'Upcoming', icon: Upcoming },
        { id: 'Food', text: 'Dashboard', icon: Food },
        { id: 'Health', text: 'Health', icon: Health },
        { id: 'Account', text: 'Account', icon: Account },
      ],
      Logo,
    };
  },
};
</script>

<style>
img {
  height: 50px;
  width: 50px;
}

.icon-section-one {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.icon-section-two {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
</style>

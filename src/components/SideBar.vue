<template>
  <div class="sidebar ps-3">
    <div class="logo mt-2 ps-5">
      <img :src="Logo" class="img-fluid" alt="logo" />
    </div>
    <!-- main logo -->
    <div class="icon-section-one ps-5 pt-5">
      <div class="col" v-for="icon in iconsListOne" :key="icon.id">
        <div class="icon-div">
          <img class="icon" :src="icon.icon" />
        </div>
        <div class="pt-3 pb-2">
          {{ icon.text }}
        </div>
      </div>
    </div>
    <div><br /><br /><br /></div>
    <div class="icon-section-two ps-5">
      <div class="col" v-for="icon in iconsListTwo" :key="icon.id">
        <div class="icon-div">
          <img class="icon" :src="icon.icon" />
        </div>
        <div class="pt-3 pb-2">
          {{ icon.text }}
        </div>
      </div>
    </div>
    <div class="footer pt-4 ps-5 ">
      <img :src="Footer" alt="footer">
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
import Footer from '../img/footer.png';

export default {
  data() {
    return {
      iconsListOne: [
        { id: 'Dashboard', text: 'Dashboard', icon: Dashboard},
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
      Footer,
    };
  },
};
</script>

<style>
.sidebar {
  background-color: #f9f9f9;
}
.icon {
  height: 25px;
  width: 25px;
}

.icon-div {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 50px;
  border-radius: 25%;
  background-color: #e6e9f2;
}

.icon-section-one,.icon-section-two {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
</style>

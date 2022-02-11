<template>
  <div class="content">
    <Search />
    <div class="cards px-5 mt-5 gap-3">
      <Card
        v-for="card in cardData"
        :key="card.id"
        :color="card.color"
        :title="card.title"
        :btc="card.btc"
        :usd="card.usd"
        :svg="card.svg"
      />
    </div>
    <!-- svg -->
    <div class="downArrow d-flex flex-row justify-content-center">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="down shadow p-3 my-5 bg-body rounded"
        width="32"
        height="32"
        viewBox="0 0 384 512"
      >
        <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
        <path
          d="M192 384c-8.188 0-16.38-3.125-22.62-9.375l-160-160c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L192 306.8l137.4-137.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-160 160C208.4 380.9 200.2 384 192 384z"
        />
      </svg>
    </div>

    <!-- activity info -->
    <div class="activity ps-5">
      <div class="title d-flex flex-column">
        <h3>Latest Activity</h3>
        <p class="text-muted fs-6">Updated 12 minutes ago</p>
      </div>
      <div class="edit d-flex flex-column justify-content-center">
        <br />
        <br />
        <p class="ps-5 text-muted text-decoration-underline">edit</p>
      </div>
      <div class="icons d-flex flex-row">
        <!-- clog -->
        <div class="clog me-3">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            height="32"
            width="32"
            fill="#888e94"
            class=""
            viewBox="0 0 512 512"
          >
            <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
            <path
              d="M495.9 166.6C499.2 175.2 496.4 184.9 489.6 191.2L446.3 230.6C447.4 238.9 448 247.4 448 256C448 264.6 447.4 273.1 446.3 281.4L489.6 320.8C496.4 327.1 499.2 336.8 495.9 345.4C491.5 357.3 486.2 368.8 480.2 379.7L475.5 387.8C468.9 398.8 461.5 409.2 453.4 419.1C447.4 426.2 437.7 428.7 428.9 425.9L373.2 408.1C359.8 418.4 344.1 427 329.2 433.6L316.7 490.7C314.7 499.7 307.7 506.1 298.5 508.5C284.7 510.8 270.5 512 255.1 512C241.5 512 227.3 510.8 213.5 508.5C204.3 506.1 197.3 499.7 195.3 490.7L182.8 433.6C167 427 152.2 418.4 138.8 408.1L83.14 425.9C74.3 428.7 64.55 426.2 58.63 419.1C50.52 409.2 43.12 398.8 36.52 387.8L31.84 379.7C25.77 368.8 20.49 357.3 16.06 345.4C12.82 336.8 15.55 327.1 22.41 320.8L65.67 281.4C64.57 273.1 64 264.6 64 256C64 247.4 64.57 238.9 65.67 230.6L22.41 191.2C15.55 184.9 12.82 175.3 16.06 166.6C20.49 154.7 25.78 143.2 31.84 132.3L36.51 124.2C43.12 113.2 50.52 102.8 58.63 92.95C64.55 85.8 74.3 83.32 83.14 86.14L138.8 103.9C152.2 93.56 167 84.96 182.8 78.43L195.3 21.33C197.3 12.25 204.3 5.04 213.5 3.51C227.3 1.201 241.5 0 256 0C270.5 0 284.7 1.201 298.5 3.51C307.7 5.04 314.7 12.25 316.7 21.33L329.2 78.43C344.1 84.96 359.8 93.56 373.2 103.9L428.9 86.14C437.7 83.32 447.4 85.8 453.4 92.95C461.5 102.8 468.9 113.2 475.5 124.2L480.2 132.3C486.2 143.2 491.5 154.7 495.9 166.6V166.6zM256 336C300.2 336 336 300.2 336 255.1C336 211.8 300.2 175.1 256 175.1C211.8 175.1 176 211.8 176 255.1C176 300.2 211.8 336 256 336z"
            />
          </svg>
        </div>

        <!-- plus icon -->
        <div
          class="plus"
          type="button"
          data-bs-toggle="modal"
          data-bs-target="#formModal"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            height="32"
            width="32"
            fill="#ffffff"
            viewBox="0 0 448 512"
          >
            <!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
            <path
              d="M432 256c0 17.69-14.33 32.01-32 32.01H256v144c0 17.69-14.33 31.99-32 31.99s-32-14.3-32-31.99v-144H48c-17.67 0-32-14.32-32-32.01s14.33-31.99 32-31.99H192v-144c0-17.69 14.33-32.01 32-32.01s32 14.32 32 32.01v144h144C417.7 224 432 238.3 432 256z"
            />
          </svg>
        </div>
      </div>
    </div>
    <ActivityInfo
      v-for="activity in activityData"
      :key="activity.id"
      :title="activity.title"
      :subtitle="activity.subtitle"
      :wallet="activity.wallet"
      :account="activity.account"
      :date="activity.date"
      :payment="activity.payment"
      :balance="activity.balance"
      :color="activity.color"
      :svg="activity.svg"
    />
  </div>

  <!-- Modal -->
  <div
    class="modal fade"
    id="formModal"
    tabindex="-1"
    aria-labelledby="formModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog modal-dialog-centered modal-sm">
      <div class="modal-content">
        <div class="modal-header justify-content-center">
          <h5 class="modal-title text-white" id="formModalLabel">
            Bill Payment
          </h5>
          <!-- <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button> -->
        </div>
        <div class="modal-body">
          <!-- select dropdown -->
          <label for="service">Service</label>
          <select
            id="service"
            class="form-select mb-4"
            aria-label="Default service example"
          >
            <option selected>Select service</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
          </select>
          <!-- wallet dropdown -->
          <label for="wallet">Wallet</label>
          <select
            id="wallet"
            class="form-select mb-4"
            aria-label="Default wallet example"
          >
            <option selected>Select wallet</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
          </select>
          <!-- amount input -->
          <label for="input">Amount</label>
          <div class="input-group mb-3">
            <input
              type="text"
              class="form-control"
              placeholder=""
              aria-label="Amount"
              aria-describedby="basic-addon1"
            />
          </div>
        </div>
        <div class="modal-footer">
          <button
            type="button"
            class="btn btn-outline-danger"
            data-bs-dismiss="modal"
          >
            Cancel
          </button>
          <button type="button" class="btn pay">Pay</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Search from '@/components/Search.vue';
import Card from '@/components/Card.vue';
import ActivityInfo from '@/components/ActivityInfo.vue';
import Bitcoin from '@/svg/bitcoin.svg';
import Ethereum from '@/svg/ethereum.svg';
import Litecoin from '@/svg/litecoin.svg';
import Insurance from '@/svg/insurance.svg';
import Electricity from '@/svg/electricity.svg';

export default {
  components: {
    Search,
    Card,
    ActivityInfo,
  },
  data() {
    return {
      cardData: [
        {
          id: 1,
          title: 'Bitcoin',
          btc: '0.2231345 BTC',
          usd: '11,032.24 USD',
          color: '#fdedd5',
          svg: Bitcoin,
        },
        {
          id: 2,
          title: 'Ethereum',
          btc: '10.612356 BTC',
          usd: '1242.31 USD',
          color: '#fde5f9',
          svg: Ethereum,
        },
        {
          id: 3,
          title: 'Litecoin',
          btc: '120.235 BTC',
          usd: '37,747.78 USD',
          color: '#b7e0e9',
          svg: Litecoin,
        },
      ],
      activityData: [
        {
          id: 'Insurance',
          title: 'Insurance',
          subtitle: 'Property Coverage',
          wallet: 'LTC Wallet',
          account: 'Personal account',
          date: '7 Jun 2021',
          payment: 'Last payment',
          balance: '-10.24 LTC',
          color:"#e8edf6",
          svg: Insurance,
        },
        {
          id: 'Electricity',
          title: 'Electricity',
          subtitle: 'Utility Payments',
          wallet: 'ETH Wallet',
          account: 'Personal account',
          date: '9 Jun 2021',
          payment: 'Last payment',
          balance: '-3.543 ETH',
          color: "#ffefe9",
          svg: Electricity,
        },
      ],
    };
  },
};
</script>

<style>
label {
  color: #52489d !important;
}
.pay {
  background-color: #52489d !important;
  color: #ffffff !important;
}
.modal-footer {
  border-top: none !important;
  display: grid !important;
  grid-template-columns: 1fr 1fr;
}
.modal-header {
  background-color: #52489d !important;
}
.clog {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 50px;
  border-radius: 25%;
  background-color: #f7f7f9;
}

.plus {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 50px;
  border-radius: 25%;
  background-color: #52489d;
}
.activity {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr !important;
}

.down {
  background-color: #ffffff;
  height: 50px;
  width: 50px;
  border-radius: 50% !important;
}
.downArrow {
  border-radius: 50%;
}
.content {
  background-color: #ffffff;
}
.cards {
  display: grid !important;
  grid-template-columns: 1fr 1fr 1fr !important;
}
</style>

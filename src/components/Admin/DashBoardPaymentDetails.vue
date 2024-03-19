<template>
  <div>
  <div style="color: white;" class="section-2-alpha">
    <p class="text-1">Payment Details</p>
    <hr/>
    <div class="form">


        <div class="separate">

          <div class="space">
            <label>Enter Bitcoin Address</label>
            <input type="text" v-model="bitcoinAddress"  class="form-input"/>
          </div>

          <!--          <div class="space">-->
          <!--            <label>Last Name</label>-->
          <!--            <input type="text"  class="form-input"/>-->
          <!--          </div>-->

        </div>

        <div class="separate">

          <div class="space">
            <label>Enter Ethereum Address</label>
            <input type="text" v-model="ethereumAddress"   class="form-input"/>
          </div>

          <!--          <div class="space">-->
          <!--            <label>Last Name</label>-->
          <!--            <input type="text"  class="form-input"/>-->
          <!--          </div>-->

        </div>

        <div class="separate">

          <div class="space">
            <label>Bank Name</label>
            <input type="text" v-model="bankName"  class="form-input"/>
          </div>


        </div>

        <div class="separate">

          <div class="space">
            <label>Account Number</label>
            <input type="text" v-model="accountNumber"  class="form-input"/>
          </div>


        </div>

        <div class="separate">

          <div class="space">
            <label>Routing Number</label>
            <input type="text" v-model="routingNumber"  class="form-input"/>
          </div>


        </div>


        <div class="btn-alpha">
          <p @click="press" class="btn">Get Current Payment details</p>
<!--          <base-button  style="  background-color: #5d78ff;border: 1px solid #5d78ff;" :loading="loading">Get Current Payment details</base-button>-->
          <br/>
<!--          <base-button style="  background-color: #5d78ff;border: 1px solid #5d78ff;" :loading="loading">Update Payment details</base-button>-->

          <p @click="update" class="btn">Update Payment details</p>

        </div>




    </div>
  </div>

  </div>
</template>

<script>
// import BaseButton from "@/components/BaseComponents/buttons/BaseButton.vue";
import StoreUtils from "@/utility/StoreUtils";
import {mapState} from "vuex";
export default {
  name: "DashBoardPaymentDetails",
  // components: {BaseButton},
  computed:{
    readPaymentWalletById() {
      return StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)
    },
    ...mapState({
      loading: state => state.paymentWallet.loading,
      auth: state => state.auth,
    }),
  },
  methods:{

    async update() {
      await StoreUtils.dispatch(StoreUtils.actions.paymentWallet.updatePaymentWallet, {
        walletId: 1,
        bitcoinAddress: this.bitcoinAddress,
        ethereumAddress: this.ethereumAddress,
        bankName: this.bankName,
        accountNumber: this.accountNumber,
        routingNumber: this.routingNumber
      })

      await StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
        walletId: 1,
      })

      await StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

      await this.populateForm()
    },

    press(){
      StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
        walletId: 1,
      })

      StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

      this.populateForm()
    },
    populateForm() {
      this.bitcoinAddress = this.readPaymentWalletById.paymentWallet.bitcoinAddress;
      this.ethereumAddress = this.readPaymentWalletById.paymentWallet.ethereumAddress;
      this.bankName = this.readPaymentWalletById.paymentWallet.bankName;
      this.accountNumber = this.readPaymentWalletById.paymentWallet.accountNumber;
      this.routingNumber = this.readPaymentWalletById.paymentWallet.routingNumber;
    },
  },
  data() {
    return {
      contacts: [],
      accountNumber: '',
      bankName: '',
      bitcoinAddress: '',
      ethereumAddress: '',
      routingNumber: '',
    };
  },
  created() {
    this.populateForm();

    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
      walletId: 1,
    })

  },

  mounted() {
    this.populateForm();

    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
      walletId: 1,
    })
  }
}
</script>

<style scoped>

.section-2-alpha{
  margin-top: 4%;
  /*float: left;*/
  /*margin-left: 20px;*/
  background-color: #0f171c;
  padding: 30px 40px;
  width: 55%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.separate{
  display: flex;
  justify-content: space-around;
}

.form-input{
  background-color: #000000;
  border: 1px solid #000000;
  border-radius: 5px ;
  width: 550px;
  height: 35px;
  color: white;
  padding: 5px 20px;
}

.text-1{
  text-align: left;
}


hr {
  border-top: 1px solid #ffffff;
  margin-bottom: 20px;
  margin-top: 20px;
}

.space{
  display: flex;
  flex-direction: column;
  text-align: left;
}
label{
  padding-bottom: 5px;
  padding-top: 25px;
}


.btn-alpha{
  /*display: flex;*/
  /*float: left;*/
  margin-top: 3%;
}

input{
  padding-top: 14px;
  padding-bottom: 14px;
  padding-left: 10px;
  background-color: rgba(247, 247, 249, 1);
  border: none;
  border-radius: 5px;
}
select{
  padding-top: 14px;
  padding-bottom: 14px;
  padding-left: 10px;
  background-color: rgba(247, 247, 249, 1);
  border: none;
  border-radius: 5px;
}

.btn{
  padding: 8px 55px;
  color: white;
  background-color: #5d78ff;
  border: 0.5px solid #5d78ff;
  border-radius: 5px;
  font-size: 13px;
  text-decoration: none;
  display: block;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}


@media (max-width: 550px) {

}
</style>

<!--<style scoped>-->
<!--.header-alpha{-->
<!--  margin-top: 4%;-->
<!--  margin-left: 3%;-->
<!--  font-size: 22px;-->
<!--  padding-bottom: 20px;-->
<!--  text-align: center;-->
<!--  color: #ffffff;-->
<!--  padding-right: 110px;-->
<!--}-->
<!--.bank-trans{-->
<!--  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);-->
<!--  background: #0f171c;-->
<!--  color: #FFFFFF;-->
<!--  margin-bottom: 1.7%;-->
<!--  margin-right: 15%;-->
<!--  margin-left: 12%;-->
<!--  padding: 32px 6% 42px;-->
<!--  border-radius: 5px;-->
<!--}-->

<!--.bank-trans-form{-->
<!--  display: flex;-->
<!--  flex-direction: column;-->
<!--  padding-bottom: 10px;-->
<!--}-->
<!--.bank-trans-header{-->
<!--  padding-bottom: 5px;-->
<!--  font-size: 20px;-->
<!--  font-weight: 700;-->
<!--  color: #ffffff;-->
<!--}-->

<!--input{-->
<!--  padding-top: 12px;-->
<!--  padding-bottom: 12px;-->
<!--  padding-left: 10px;-->
<!--  background-color: #000000;-->
<!--  border: none;-->
<!--  border-radius: 5px;-->
<!--}-->

<!--label{-->
<!--  padding-top: 7px;-->
<!--  padding-bottom: 17px;-->
<!--  font-size: 15px;-->
<!--  color: #ffffff;-->
<!--  font-weight: 700;-->
<!--  /*display: none;*/-->
<!--}-->

<!--.bank-trans-btn{-->
<!--  margin-bottom: 4%;-->
<!--  padding: 13px 100px;-->
<!--  color: white;-->
<!--  background-color: #D23535;-->
<!--  border-color: #D23535;-->
<!--  border-radius: 5px;-->
<!--  font-size: 16px;-->
<!--  display: block;-->
<!--  margin-right: auto;-->
<!--  margin-left: auto;-->
<!--}-->

<!--.bank-trans-btn:hover{-->
<!--  color: #071333;-->
<!--  background-color: #ffffff;-->
<!--  border-color: #D23535;-->
<!--  -webkit-transition: all 0.35s ease;-->
<!--  transition: all 0.35s ease;-->
<!--}-->

<!--.reduce{-->
<!--  margin-left: 33%;-->
<!--  margin-right: 33%;-->
<!--  margin-top: 3%;-->
<!--}-->


<!--@media (max-width: 990px) {-->
<!--  .header-alpha{-->
<!--    font-size: 20px;-->
<!--    margin-top: unset;-->
<!--  }-->

<!--  .bank-trans{-->
<!--    padding: 20px 5% 35px;-->
<!--    border-radius: 15px;-->
<!--    margin-left: unset;-->
<!--    margin-right: unset;-->
<!--  }-->

<!--  .bank-trans-header{-->
<!--    font-size: 20px;-->
<!--  }-->

<!--  .bank-trans-btn{-->
<!--    margin-bottom: 6%;-->
<!--    padding: 14px 80px;-->
<!--    font-size: 15px;-->
<!--  }-->
<!--}-->

<!--</style>-->
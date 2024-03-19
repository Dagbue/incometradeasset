<template>
  <div class="alpha">
    <div class="image">
      <img src="@/assets/successcheck.svg" alt="fether">
    </div>

    <div class="text-area">
      <h3>Login success🥳</h3>
      <p>You have successfully Logged in to your<br/>
        Income Trade Asset account</p>
    </div>

    <div class="submit">
      <button class="submit-btn"  @click="signIn">Proceed to DashBoard</button>
    </div>

  </div>
</template>

<script>

import {mapState} from "vuex";
import StoreUtils from "@/utility/StoreUtils";
import router from "@/router";


export default {
  name: "SignInSuccess",
  data() {
    return {
      userId: "",
      userInfo: "",
    };
  },
  computed:{
    ...mapState({
      loading: state => state.auth.loading,
      auth: state => state.auth,
    }),
    userDetails() {
      return StoreUtils.rootGetters(StoreUtils.getters.auth.getUserInfo)
    },
    userTrade() {
      return StoreUtils.rootGetters(StoreUtils.getters.trade.getReadUserTrade)
    }
  },
  methods:{
    async signIn() {
      await this.localStore()
      await router.push("/over-view")
    },

    localStore(){
      localStorage.userId = this.userDetails.user.userId
      localStorage.userFirstName = this.userDetails.user.firstName
      localStorage.userLastName = this.userDetails.user.lastName
      localStorage.setItem('userInfo', JSON.stringify(this.userDetails.user));
      localStorage.setItem('userTrade', JSON.stringify(this.userTrade.trades));
    },
  },
  // created() {
  //   this.userId = localStorage.getItem('userId')
  //
  //   // Retrieve the object from local storage
  //   const storedObject = localStorage.getItem('userInfo');
  //
  //   if (storedObject) {
  //     this.userInfo = JSON.parse(storedObject);
  //   }
  //
  //   StoreUtils.rootGetters(StoreUtils.getters.auth.getReadUserById)
  // },
  //
  // mounted() {
  //
  //   this.userId = localStorage.getItem('userId')
  //
  //   // Retrieve the object from local storage
  //   const storedObject = localStorage.getItem('userInfo');
  //
  //   if (storedObject) {
  //     this.userInfo = JSON.parse(storedObject);
  //   }
  //
  //   StoreUtils.dispatch(StoreUtils.actions.auth.readReadUserById, {
  //     userId : localStorage.getItem('userId')
  //   })
  // }
}
</script>

<style scoped>
.alpha{
  margin-top: 14%;
}


.text-area h3{
  padding-bottom: 0;
  margin-bottom: 0;
  text-align: center;
  letter-spacing: 0.5px;
  color: #101828;
  font-weight: 600;
  font-size: 21px;
  line-height: 30px;
}

.text-area p{
  padding-top: 2px;
  margin-top: 2px;
  text-align: center;
  letter-spacing: 0.5px;
  color: #667085;
  font-weight: 400;
  font-size: 14px;
  line-height: 24px;
}

.text-area{
  margin-bottom: 1%;
}
.image{
  display: flex;
  justify-content: center;
  margin-bottom: 0.8%;
}

.submit{
  display: flex;
  justify-content: center;
  margin-top: 1.5%;
}

.submit-btn{
  background-color: #0f171c;
  border: 1px solid #0f171c;
  border-bottom-color: transparent;
  border-right-color: transparent;
  color: #ffffff;
  padding: 12px 10% 12px 10%;
  border-radius: 5px;
}

.submit-btn:hover{
  box-shadow: 0 0 7px rgba(0, 0, 0, 0.7);
}
</style>
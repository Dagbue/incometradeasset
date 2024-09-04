<template>
  <div class="alpha">
    <div class="section-alpha-1">
      <p class="section-header-1">Choose an Investment Plan</p>
      <p class="section-header">You don't have an account yet? start trading with Coin Matrix Investment.</p>
    </div>

    <div class="section-alpha">

      <div class="third-section top">
        <p class="text-1">Basic</p>
        <p class="text-2">10<span class="text-2-inner">%</span></p>
        <!--        <p class="text-2">4 Months</p>-->
        <p class="text-3">4 Months</p>

        <div class="btn" >
          <p>Invest Now</p>
        </div>

        <div class="separate">
          <p>$500 MINIMUM DEPOSIT</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>ENHANCED SECURITY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>1.3% DAILY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>GUARANTEED ROI</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>24/7 SUPPORT</p>
          <i class='bx bxs-info-circle'></i>
        </div>
      </div>

      <div class="third-section top">
        <p class="text-1">Standard</p>
        <p class="text-2">20<span class="text-2-inner">%</span></p>
        <!--        <p class="text-2">4 Months</p>-->
        <p class="text-3">8 Months</p>

        <div class="btn" >
          <p>Invest Now</p>
        </div>

        <div class="separate">
          <p>$10,000 MINIMUM DEPOSIT</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>ENHANCED SECURITY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>1.5% DAILY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>GUARANTEED ROI</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>24/7 SUPPORT</p>
          <i class='bx bxs-info-circle'></i>
        </div>
      </div>

      <div class="third-section top">
        <p class="text-1">Premium</p>
        <p class="text-2">30<span class="text-2-inner">%</span></p>
        <!--        <p class="text-2">4 Months</p>-->
        <p class="text-3">12 Months</p>

        <div class="btn" >
          <p>Invest Now</p>
        </div>

        <div class="separate">
          <p>$50,000 MINIMUM DEPOSIT</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>ENHANCED SECURITY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>1.8% DAILY</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>GUARANTEED ROI</p>
          <i class='bx bxs-info-circle'></i>
        </div>

        <div class="separate">
          <p>24/7 SUPPORT</p>
          <i class='bx bxs-info-circle'></i>
        </div>
      </div>

<!--      <div class="third-section top">-->
<!--        <p class="text-1">Premium</p>-->
<!--        <p class="text-2">30<span class="text-2-inner">%</span></p>-->
<!--        &lt;!&ndash;        <p class="text-2">4 Months</p>&ndash;&gt;-->
<!--        <p class="text-3">24 Months</p>-->

<!--        <div class="btn" >-->
<!--          <p>Invest Now</p>-->
<!--        </div>-->

<!--        <div class="separate">-->
<!--          <p>$5,000 MINIMUM DEPOSIT</p>-->
<!--          <i class='bx bxs-info-circle'></i>-->
<!--        </div>-->

<!--        <div class="separate">-->
<!--          <p>ENHANCED SECURITY</p>-->
<!--          <i class='bx bxs-info-circle'></i>-->
<!--        </div>-->

<!--        <div class="separate">-->
<!--          <p>1.8% DAILY</p>-->
<!--          <i class='bx bxs-info-circle'></i>-->
<!--        </div>-->

<!--        <div class="separate">-->
<!--          <p>GUARANTEED ROI</p>-->
<!--          <i class='bx bxs-info-circle'></i>-->
<!--        </div>-->

<!--        <div class="separate">-->
<!--          <p>24/7 SUPPORT</p>-->
<!--          <i class='bx bxs-info-circle'></i>-->
<!--        </div>-->
<!--      </div>-->

    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection6",
  methods: {
    onPostClick() {
      this.$router.push("/register");
      window.scrollTo(0, 0);
    },
  },
}
</script>

<style scoped>

.alpha{
  padding-top: 5%;
  /*padding-bottom: 3%;*/
}
.section-header{
  font-size: 17px;
  color: #0f171c;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
}
.section-header-1{
  font-size: 30px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 1%;
}
.section-alpha{
  display: flex;
  justify-content: space-evenly;
  margin-right: 3%;
  margin-left: 3%;
}

.section-alpha-2{
  display: flex;
  justify-content: space-evenly;
}

.section-alpha-1{
  display: block;
  text-align: center;
  margin-bottom: 2%;
}

.third-section{
  width: 350px;
  height: 480px;
  background-color: #ffffff;
  box-shadow:  20px 20px 60px #d9d9d9,
  -20px -20px 60px #ffffff;
  border-radius: 8px;
  margin-bottom: 5%;
}

.separate{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  margin-top: 1%;
}

.separate i{
  padding-top: 15px;
  padding-right: 13px;
}

.separate p{
  width: 220px;
  padding-top: 15px;
  font-size: 14px;
  line-height: 24px;
  color: #667085;
  padding-left: 13px;
}

.btn{
  margin-top: 5%;
  margin-bottom: 1%;
}

.btn p{
  display: block;
  margin-left: auto;
  margin-right: auto;
  align-items: center;
  padding: 12px 20px;
  gap: 8px;
  width: 180px;
  height: 44px;
  background: #0f171c;
  border: 1px solid #0f171c;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 4px;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #FFFFFF;
  text-align: center;
}

.btn p:hover{
  background-color: #ccaa16;
  color: #ffffff;
  border: 1px solid #ccaa16;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
}

.top{
  margin-top: 1%;
}

.text-1{
  text-align: center;
  padding-top: 9%;
  padding-bottom: 3%;
  font-size: 19px;
}

.text-2{
  text-align: center;
  padding-bottom: 4%;
  font-size: 27px;
  font-weight: bold;
}

.text-2-inner{
  font-size: 14px;
  font-weight: normal;
}

.text-3{
  text-align: center;
  font-size: 16px;
  width: 70%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}


.bx{
  color: #ccaa16;
}
@media (max-width: 990px) {

}

@media (max-width: 700px) {
  .section-alpha{
    display: block;
    /*margin-left: 21%;*/
    margin-top: 3.5%;
  }
  .section-alpha-2{
    display: block;
    /*margin-left: 21%;*/
    margin-top: 3.5%;
  }
  .third-section{
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .section-header-1{
    font-size: 27px;
  }

  .section-header{
    margin-left: 3%;
    margin-right: 3%;
  }
}

@media (max-width: 500px) {
}

</style>
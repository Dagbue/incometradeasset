<template>
  <div class="alpha">

    <div class="section-alpha">
      <div class="section-1">
        <h2 class="text-1">Get Started</h2>
        <p class="text-2">Start Trading with Ease on Our Platform</p>
        <div class="btn-part">
          <p class="btn-1" @click="onPostClick2">Learn More</p>
          <p class="btn-2" @click="onPostClick">Sign Up</p>
        </div>
      </div>

      <div class="section-2">

        <div class="timeline">
          <div class="timeline-object complete">
            <div class="timeline-status">
              <i class="fas fa-tarp"></i>
            </div>
            <div class="timeline-content">
              <h3>Step One</h3>
              <span>Create an account and deposit funds to get started.</span>
            </div>
          </div>
          <div class="timeline-object complete">
            <div class="timeline-status">
              <i class="fas fa-project-diagram"></i>
            </div>
            <div class="timeline-content">
              <h3>Step Two</h3>
              <span>Choose the currency pairs you want to trade.</span>
            </div>
          </div>
          <div class="timeline-object complete">
            <div class="timeline-status">
              <i class="fas fa-project-diagram"></i>
            </div>
            <div class="timeline-content">
              <h3>Step Three</h3>
              <span>Analyze market trends and make informed trading decisions.</span>
            </div>
          </div>
          <div class="timeline-object">
            <div class="timeline-status">
              <i class="fas fa-graduation-cap" style="color: #0f171c;"></i>
            </div>
            <div class="timeline-content">
              <h3>Step Four</h3>
              <span>Execute trades and monitor your portfolio performance.</span>
            </div>
          </div>
        </div>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "HomeSection2",
  methods: {
    onPostClick() {
      this.$router.push("/register");
    },
    onPostClick2() {
      this.$router.push("/about");
    },
  },
}
</script>

<style scoped>
.section-alpha{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: space-evenly;
  padding-top: 5%;
  padding-bottom: 5%;
  /*background-color: #f4f5f6;*/
}

.btn-part{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: left;
  padding-top: 4%;
  padding-bottom: 2%;
}

.text-1{
  color: #071333;
  padding-bottom: 2%;
  font-weight: 900;
}

.text-2{
  font-size: 25px;
  color: #0f171c;
}


:root{
  --main-clr: #8c8;
  --white: #fff;
  --black: #1a1b1c;
  --light-clr: #7a7b7c;
  --light-bg: #e1f1d1;
  --red: #ff4754;
}



.timeline-object{
  display: flex;
  align-items: center;
  margin-top: 50px;
  position: relative;
}

.timeline-object.complete::before {
  content: '';
  display: block;
  position: absolute;

  width: 3px;
  height: 100px;
  background: #0f171c;

  left: 18px;
  top: 40px;
  transform: translateX(-50%);
  z-index: -1;
}
.timeline-status{
  height: 36px;
  width: 36px;
  border-radius: .5rem;
  background: #0f171c;
  padding-top: 3px;
}
.timeline-status i{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  color: #FFFFFF;
}

.timeline-object:not(.complete) .timeline-status{
  background: var(--white);
  border: 4px solid #c5c5c5;
}

.timeline-content{
  margin-left: 15px;
}

.timeline-content h3{
  color: #345;
  padding: 5px 10px;
  border-radius: 5px;
  margin-bottom: 10px;
}

.timeline-content span{
  color: #103b27;
  font-size: .9rem;
  font-weight: lighter;
}

.timeline-object:not(.complete) .timeline-content h3{
  color: #8a8a8a;
  background: rgba(245, 245, 245, .3);
}

.btn-1{
  background: #0f171c;
  border: 1.5px solid #0f171c;
  padding: 8px 25px;
  margin-right: 3%;
  color: #ffffff;
  width: 150px;
  text-align: center;
  border-radius: 4px;
}

.btn-1:hover{
  background: #ccaa16;
  border: 1.5px solid #ccaa16;
  color: #ffffff;
  padding: 8px 25px;
  margin-right: 3%;
  width: 150px;
  text-align: center
}

.btn-2{
  background: #ccaa16;
  border: 1.5px solid #ccaa16;
  color: #ffffff;
  padding: 8px 25px;
  margin-right: 3%;
  width: 150px;
  text-align: center;
  border-radius: 4px;
}

.btn-2:hover{
  background: #0f171c;
  border: 1.5px solid #0f171c;
  color: #ffffff;
  padding: 8px 25px;
  margin-right: 3%;
  width: 150px;
  text-align: center;
}


@media (max-width: 990px) {

}

@media (max-width: 700px){
  .section-alpha{
    display: block;
    margin-left: auto;
    margin-right: auto;
    padding-top: 10%;
    padding-bottom: 10%;
  }

  .section-1{
    text-align: center;
  }


  .section-2{
    margin-left: 5%;
  }


  .btn-part{
    justify-content: center;
  }


}

@media (max-width: 500px){


  .text-2{
    font-size: 19px;
  }
}

</style>
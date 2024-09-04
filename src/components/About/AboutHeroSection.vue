<template>
  <div class="alpha">

    <main>

      <div class="main-intro">
    <h1> Why choose <br> Coin Matrix <br> Investment </h1>
    <p> Maximize your trading success with our superior, <br> market conditions, offering you the optimal <br> advantage for financial excellence.</p>
    <p class="btn">Register</p>
  </div>

      <div class="main-quotes">
        <p>"We aim to deliver the ultimate online trading experience <br> by passionately innovating and continually enhancing <br> the way you invest in financial markets."</p>

        <p>"We aim is to deliver an unparalleled trading experience <br> by passionately innovating and enhancing how <br> you invest in financial markets online."</p>
      </div>

    </main>

  </div>
</template>

<script>
export default {
  name: "AboutHeroSection"
}
</script>

<style scoped>
h1{
  font-size: 24px;
  line-height: 32px;
  color: #ffffff;
  font-weight: 600;
  /*text-transform: uppercase;*/
}
p{
  font-size: 14px;
  line-height: 18px;
  color: #ffffff;
}
main{
  width: 100%;
  height: 80vh;
  background-color: #0f171c;
  background-image: url("@/assets/hero.png");
  background-size: 50vh, cover;
  background-repeat: no-repeat;
  background-position: bottom, center;
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  /*column-gap: 20px;*/
  z-index: 100;
}

main .main-intro h1 {
  font-size: 53px;
  line-height: 55px;
  letter-spacing: 1.8px;
  padding-bottom: 5px;
}

main  p {
  font-size: 18px;
  line-height: 30px;
}

.btn{
  margin-top: 15px;
  font-size: 18px;
  display: block;
  background-color: #ccaa16;
  color: #FFFFFF;
  padding: 5px 30px;
  width: fit-content;
  border-radius: 4px;
}

main .main-quotes p {
  /*border-left: 4px solid #ffcf01;*/
  padding-left: 20px;
  margin: 40px;
}

main .main-quotes p:nth-child(2){
  margin-left: 120px;
}

main .main-intro  {
  position: relative;
  right: 4vh;
  padding-bottom: 8vh;
}

main .main-quotes  {
  position: relative;
  left: 18vh;
}


@keyframes showContent {
  to{
    transform: translateY(0);
    filter: blur(0);
    opacity: 1;
  }
}

main .main-intro h1,
main p{
  transform: translateY(30px);
  filter: blur(20px);
  opacity: 0;
  animation: showContent .4s .6s ease-in-out 1 forwards;
}

main .main-intro h1{
  animation-delay: 0.8s;
}

main p{
  animation-duration: 1.2s;
}

@media screen and (max-width: 980px) {

}

@media screen and (max-width: 760px) {
  main .main-intro h1 {
    font-size: 35px;
    line-height: 35px;
    letter-spacing: 1.5px;
  }

  main{
    background-size: 45vh, cover;
  }



  main .main-quotes p:nth-child(2){
    margin-left: unset;
  }

  main .main-intro  {
    position: relative;
    right: unset;
    padding-bottom: unset;
    left: 4vh;
  }

  main .main-quotes  {
    position: relative;
    left: unset;
  }

  main  p {
    font-size: 17px;
    line-height: 25px;
  }


}

@media screen and (max-width: 500px) {

}
</style>
<template>
  <div class="alpha">

    <div class="section-1">
      <h2 class="text-1" style="text-align: center;">Powerful web and mobile trading platforms.</h2>
      <img src="https://assets.cmcmarkets.com/images/platform_device_cluster_group_extra.png" alt="" class="image"/>
      <div class="section-1-inner">


        <div class="section-1-inner-content">
          <i class='bx bx-tab'></i>
          <p>Tablet</p>
        </div>

        <div class="section-1-inner-content">
          <i class='bx bx-mobile'></i>
          <p>Phone</p>
        </div>

        <div class="section-1-inner-content">
          <i class='bx bx-laptop' ></i>
          <p>Laptop</p>
        </div>


      </div>

      <p class="text-2" style="text-align: center;">Coming Soon On</p>

      <div class="image-part">
        <img src="https://assets.cmcmarkets.com/images/apple-app-store_extra.webp" alt="" class="image2" />

        <img src="https://assets.cmcmarkets.com/images/google-play_extra.jpg" alt="" class="image2" />
      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: "HomeSection5"
}
</script>

<style scoped>
.alpha{
  padding-top: 5%;
  padding-bottom: 5%;
  background: #f4f5f6;
}
.section-1-inner{
  display: flex;
  justify-content: center;
  gap: 20px;
}
.section-1-inner-content{
  text-align: center;
}
.section-1-inner-content p{
  font-size: 17px;
}
.image{
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.text-1{
  padding-bottom: 2.5%;
  font-size: 25px;
}
.text-2{
  padding-top: 1%;
  font-size: 23px;
}
.bx{
  font-size: 30px;
  margin-top: 10px;
}

.image-part{
  display: flex;
  justify-content: center;
  margin-top: 15px;
  gap: 20px;
}



@media (max-width: 990px){

  .image{
    width: 100%;
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-top: 3%;
  }


  .image2{
    width: 25%;
  }


}

@media (max-width: 500px){

}
</style>
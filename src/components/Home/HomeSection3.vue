<template>
  <div class="alpha">

    <div id="page" class="site">
      <div class="container">
        <div class="testi">
          <div class="head">
            <h2 style="text-align: center;">Testimonials.</h2>
            <p style="text-align: center; color: #667085;">See what people are saying...</p>
          </div>

          <div v-show="!mobile" class="body swiper">
            <ul style="list-style: none;">
              <li>
                <div class="wrapper">
                  <div class="thumbnail">
                    <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/xl_exness_security1_222430ca3c.jpg" alt="" class=""/>
                  </div>
                  <div class="aside">
                    <p>
                      The overall experience is exceptional, characterized by outstanding satisfaction. The financial
                      rewards, including both profits and bonuses, are truly remarkable and exceed expectations,
                      creating a sense of awe and astonishment.</p>
                    <div class="name">
                      <h4>Jason Adams</h4>
                      <p>Trader</p>
                    </div>
                  </div>
                </div>
              </li>
              <li>
                <div class="wrapper mobile">
                  <div class="aside">
                    <p>The interface is incredibly intuitive, making navigation a breeze, and its user-friendly design
                      adds to the overall experience. Using it feels as effortless as generating income effortlessly,
                      almost like earning in my sleep.</p>
                    <div class="name">
                      <h4>Charles Linda</h4>
                      <p>Investor</p>
                    </div>
                  </div>
                  <div class="thumbnail">
                    <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/exness_constantina_georgiadou_dacdbefeca.png" alt="" class=""/>
                  </div>
                </div>
              </li>
              <li>
                <div class="wrapper">
                  <div class="thumbnail">
                    <img src="https://media.istockphoto.com/id/1435745704/photo/portrait-of-smiling-mid-adult-businessman-standing-at-corporate-office.webp?b=1&s=612x612&w=0&k=20&c=Kjs_YBhIVk_P71Q-oeIF85CiK5B0so_aOSPif2PFwRI=" alt="" class=""/>
                  </div>
                  <div class="aside">
                    <p>
                      The website offers an exceptional user experience, providing a range of valuable services.
                      The customer service is highly responsive and efficient, ensuring prompt assistance and support
                      to enhance overall satisfaction.</p>
                    <div class="name">
                      <h4>David Gill</h4>
                      <p>Programmer</p>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </div>

          <div v-show="mobile" class="body swiper">
            <ul style="list-style: none;">
              <li>
                <div class="wrapper">
                  <div class="thumbnail">
                    <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/xl_exness_security1_222430ca3c.jpg" alt="" class=""/>
                  </div>
                  <div class="aside">
                    <p>
                      The overall experience is exceptional, characterized by outstanding satisfaction. The financial
                      rewards, including both profits and bonuses, are truly remarkable and exceed expectations,
                      creating a sense of awe and astonishment.</p>
                    <div class="name">
                      <h4>Jason Adams</h4>
                      <p>Trader</p>
                    </div>
                  </div>
                </div>
              </li>
              <li>
                <div class="wrapper mobile">
                  <div class="thumbnail">
                    <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/exness_constantina_georgiadou_dacdbefeca.png" alt="" class=""/>
                  </div>
                  <div class="aside">
                    <p>The interface is incredibly intuitive, making navigation a breeze, and its user-friendly design
                      adds to the overall experience. Using it feels as effortless as generating income effortlessly,
                      almost like earning in my sleep.</p>
                    <div class="name">
                      <h4>Charles Linda</h4>
                      <p>Investor</p>
                    </div>
                  </div>
                </div>
              </li>
              <li>
                <div class="wrapper">
                  <div class="thumbnail">
                    <img src="https://media.istockphoto.com/id/1435745704/photo/portrait-of-smiling-mid-adult-businessman-standing-at-corporate-office.webp?b=1&s=612x612&w=0&k=20&c=Kjs_YBhIVk_P71Q-oeIF85CiK5B0so_aOSPif2PFwRI=" alt="" class=""/>
                  </div>
                  <div class="aside">
                    <p>
                      The website offers an exceptional user experience, providing a range of valuable services.
                      The customer service is highly responsive and efficient, ensuring prompt assistance and support
                      to enhance overall satisfaction.</p>
                    <div class="name">
                      <h4>David Gill</h4>
                      <p>Programmer</p>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </div>

        </div>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: "HomeSection3",
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSwiper,
      onSlideChange,
    };
  },

  data()  {
    return {
      mobile: false,
      mobileNav: false,
      windowWidth: false,
    }
  },
  created() {
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen();
  },
  methods: {
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 800){
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
  }
}
</script>

<style scoped>
:root {
  --primary-color: #ffcf01;
  --white-color: #ffffff;
  --light-color: #ced6e0;
  --dark-color: #2f3542;
  --box-shadow: rgb(0 0 2 / 35%) 0 20px 30px -10px;
}
.alpha{
  padding-top: 3%;
  padding-bottom: 3%;
  background: #f4f5f6;
}

.site{
  /*height: 100vh;*/
  display: flex;
  align-items: center;
  justify-content: center;
}

.container{
  max-width: 1100px;
  width: 100%;
  padding: 0 30px;
  margin: 0 auto;
}

.testi{
  max-width: 900px;
  margin: 0 auto;
}

.testi head {
  text-align: center;
  margin-bottom: 60px;
}

.testi head h2 {
  font-size: 40px;
  font-weight: 800;
}


.testi .wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 60px;
  padding: 30px 0;
}

.testi .thumbnail{
  width: 150px;
  height: 150px;
  position: relative;
  flex-shrink: 0;
}

.testi .thumbnail::before{
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: calc(100% + 30px);
  height: calc(100% + 10px);
  background-color: var(--primary-color);
  border-radius: 33% 67% 50% 50% / 50% 14% 86% 50%;
  z-index: -1;
  box-shadow: var(--box-shadow);
}

.testi .thumbnail img{
  object-fit: cover;
  width: 100%;
  height: 100%;
  border-radius: 50%;
}

.wrapper{
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 60px;
  padding: 30px 0;
}

.testi .aside{
  position: relative;
  padding-top: 15px;
  display: flex;
  flex-direction: column;
  align-self: flex-end;
}


.testi .aside > p{
  position: relative;
  font-size: 14px;
  line-height: normal;
  margin-bottom: 30px;
}

.testi .aside > p::before,
.testi .aside > p::after{
  font-size: 80px;
  font-weight: 800;
  line-height: 1;
  position: absolute;
  color: var(--light-color);
  height: 40px;
  z-index: -1;
}

.testi .aside > p::before{
  content: open-quote;
  top: -40px;
  left: 10px;
}

.testi .aside > p::after{
  content: close-quote;
  right: 0;
}

.testi .aside .name{
  position: relative;
  width: fit-content;
  line-height: 1;
}

.testi .aside .name h4{
  font-size: 22px;
  font-weight: 800;
  color: #0f171c;
  opacity: .8;
}

.testi .aside .name p{
  font-size: 12px;
  text-align: right;
}

.testi :is(.swiper-button-next, .swiper-button-prev){
  background-color: var(--light-color);
  top: 35%;
  width: 38px;
  height: 38px;
  border-radius: 50%;
  transition: background-color .3s;
  box-shadow: var(--box-shadow);
}

.testi :is(.swiper-button-next, .swiper-button-prev):hover{
  background-color: var(--primary-color);
}

.testi :is(.swiper-button-next, .swiper-button-prev)::after{
  font-size: 16px;
  font-weight: 800;
  color: var(--white-color);
}

.testi .swiper-pagination {
  position: relative;
}

.testi .swiper-pagination span {
  background-color: var(--light-color);
}
@media screen and (min-width: 800px){
  .testi .wrapper{
    flex-direction: row;
    padding: 30px 100px;
  }

  .testi .thumbnail{
    width: 200px;
    height: 200px;
    position: relative;
    flex-shrink: 0;
  }

  .testi :is(.swiper-button-next, .swiper-button-prev){
    top: 50%;
  }

  .alpha{
    padding-top: 10%;
    padding-bottom: 10%;
  }


}
</style>
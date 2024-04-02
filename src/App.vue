<template>
  <div class="alpha">
    <navigation-view/>
    <!--    <a href="https://wa.me/15102569690?text="  target="_blank" class="whatsapp_float">-->
    <!--      <i class='bx bxl-whatsapp'></i>-->
    <!--    </a>-->

<!--        <router-view v-slot="{ Component }">-->
<!--          <transition name="route" mode="out-in">-->
<!--            <component :is="Component"></component>-->
<!--          </transition>-->
<!--        </router-view>-->

    <transition name="slide-fade" mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>


<script>
import NavigationView from "@/components/BaseComponents/NavigationView.vue";
import Toastify from 'toastify-js'
import 'toastify-js/src/toastify.css'

export default {
  components: {NavigationView},
  data() {
    return {
      messages: [
        " 🇩🇿 John made a deposit of $2000",
        " 🇮🇹 Ivan made a deposit of $1660",
        " 🇪🇸 Evan made a deposit of $3531",
        " 🇺🇸 Rachel made a deposit of $3006",
        " 🇮🇳 Quinn made a withdrawal of $1557",
        " 🇪🇸 Fiona made a deposit of $2544",
        " 🇨🇳 Ivan made a withdrawal of $4558",
        " 🇺🇸 Evan made a deposit of $3435",
        " 🇲🇽 Diana made a withdrawal of $2681",
        " 🇲🇽 Quinn made a deposit of $3959",
        " 🇿🇦 Bob made a deposit of $661",
        " 🇦🇪 Oscar made a deposit of $1876",
        " 🇷🇺 Penny made a deposit of $868",
        " 🇩🇪 Evan made a withdrawal of $2741",
        " 🇷🇺 Fiona made a withdrawal of $4856",
        " 🇺🇸 Charlie made a deposit of $1231",
        " 🇧🇷 Charlie made a withdrawal of $4588",
        " 🇨🇦 Steve made a withdrawal of $3108",
        " 🇸🇬 Steve made a withdrawal of $2178",
        " 🇦🇪 Linda made a deposit of $3055",
        " 🇦🇪 Steve made a deposit of $2300",
        " 🇦🇪 Evan made a withdrawal of $1543",
        " 🇰🇷 Ivan made a withdrawal of $1399",
        " 🇯🇵 Evan made a deposit of $643",
        " 🇸🇬 Linda made a withdrawal of $1400",
        " 🇺🇸 Rachel made a withdrawal of $3195",
        " 🇷🇺 Oscar made a withdrawal of $1066",
        " 🇳🇿 Julia made a deposit of $2064",
        " 🇬🇧 Steve made a withdrawal of $4305",
        " 🇬🇧 Penny made a deposit of $1892",
        " 🇫🇷 Mike made a withdrawal of $922",
        " 🇯🇵 Hannah made a deposit of $2999",
        " 🇨🇳 Ivan made a deposit of $453",
        " 🇮🇹 Steve made a deposit of $4687",
        " 🇨🇦 Charlie made a deposit of $1595",
        " 🇦🇪 George made a deposit of $2162",
        " 🇪🇸 George made a withdrawal of $4518",
        " 🇨🇦 Fiona made a withdrawal of $647",
        " 🇦🇪 Steve made a withdrawal of $326",
        " 🇮🇳 Bob made a deposit of $3433",
        " 🇷🇺 Ivan made a deposit of $302",
        " 🇸🇬 Alice made a withdrawal of $3275",
        " 🇧🇷 Oscar made a deposit of $2369",
        " 🇦🇺 Quinn made a deposit of $1568",
        " 🇸🇦 Steve made a deposit of $4705",
        " 🇫🇷 Ivan made a deposit of $1695",
        " 🇫🇷 Steve made a withdrawal of $3344",
        " 🇿🇦 Hannah made a deposit of $612",
        " 🇲🇽 Linda made a deposit of $4479",
        " 🇧🇷 Nora made a withdrawal of $4064",
        " 🇰🇷 Nora made a withdrawal of $2621",
        " 🇦🇪 Fiona made a withdrawal of $2300",
        " 🇦🇪 Hannah made a deposit of $1046",
        " 🇸🇬 Steve made a deposit of $388",
        " 🇳🇿 Diana made a withdrawal of $2489",
        " 🇯🇵 Linda made a withdrawal of $574",
        " 🇰🇷 Linda made a withdrawal of $548",
        " 🇮🇹 Linda made a withdrawal of $1252",
        " 🇫🇷 George made a deposit of $2971",
        " 🇨🇳 Rachel made a deposit of $1431",
        " 🇨🇦 Bob made a withdrawal of $4949",
        " 🇩🇪 George made a withdrawal of $1553",
        " 🇳🇿 Ivan made a deposit of $3236",
        " 🇺🇸 Alice made a deposit of $1766",
        " 🇪🇸 Alice made a deposit of $4021",
        " 🇦🇪 Oscar made a withdrawal of $881",
        " 🇮🇳 Tina made a withdrawal of $3371",
        " 🇨🇳 Julia made a deposit of $4346",
        " 🇦🇺 Mike made a withdrawal of $1110",
        " 🇸🇦 Nora made a deposit of $1525",
        " 🇿🇦 Hannah made a deposit of $2797",
        " 🇩🇪 Hannah made a withdrawal of $4566",
        " 🇩🇪 Diana made a deposit of $917",
        " 🇦🇺 Hannah made a deposit of $580",
        " 🇺🇸 Rachel made a deposit of $2945",
        " 🇨🇳 Mike made a deposit of $1717",
        " 🇺🇸 Evan made a withdrawal of $3016",
        " 🇦🇺 Evan made a withdrawal of $2508",
        " 🇮🇳 Linda made a withdrawal of $3160",
        " 🇷🇺 Mike made a withdrawal of $601",
        " 🇫🇷 Ivan made a deposit of $577",
        " 🇦🇪 Oscar made a deposit of $1766",
        " 🇬🇧 Fiona made a withdrawal of $3440",
        " 🇿🇦 Fiona made a deposit of $3965",
        " 🇦🇺 Mike made a deposit of $4023",
        " 🇮🇹 Diana made a withdrawal of $203",
        " 🇩🇪 Evan made a withdrawal of $1619",
        " 🇪🇸 Quinn made a deposit of $1474",
        " 🇩🇪 Hannah made a deposit of $362",
        " 🇨🇳 Linda made a withdrawal of $860",
        " 🇿🇦 Hannah made a deposit of $1894",
        " 🇨🇳 Mike made a withdrawal of $4620",
        " 🇬🇧 Rachel made a deposit of $2911",
        " 🇸🇦 Charlie made a deposit of $3349",
        " 🇩🇪 Mike made a withdrawal of $1159",
        " 🇨🇳 Evan made a withdrawal of $1101",
        " 🇯🇵 Diana made a deposit of $2138",
        " 🇫🇷 Diana made a withdrawal of $2020",
        " 🇦🇺 Penny made a withdrawal of $2152",
        " 🇲🇽 Nora made a deposit of $2379",
        " 🇸🇦 Quinn made a withdrawal of $2295"
      ],
      currentMessageIndex: 0, // Track the current message index
    };
  },
  methods: {
    // showToast() {
    //   Toastify({
    //     text: "This is a toast",
    //     duration: 5000,
    //     destination: "https://github.com/apvarun/toastify-js",
    //     newWindow: true,
    //     close: true,
    //     gravity: "bottom", // `top` or `bottom`
    //     position: "left", // `left`, `center` or `right`
    //     stopOnFocus: true, // Prevents dismissing of toast on hover
    //     style: {
    //       background: "linear-gradient(to right, grey, grey)",
    //       width: "400px"
    //     },
    //   }).showToast();
    // },
    // showToast() {
    //   // Define the interval duration in milliseconds (e.g., every 10 seconds)
    //   const intervalDuration = 10000;
    //
    //   setInterval(() => {
    //     Toastify({
    //       text: "This is a toast",
    //       duration: 5000,
    //       destination: "https://github.com/apvarun/toastify-js",
    //       newWindow: true,
    //       close: true,
    //       gravity: "bottom", // `top` or `bottom`
    //       position: "left", // `left`, `center` or `right`
    //       stopOnFocus: true, // Prevents dismissing of toast on hover
    //       style: {
    //         background: "linear-gradient(to right, grey, grey)",
    //         width: "400px"
    //       },
    //     }).showToast();
    //   }, intervalDuration);
    // }

     shuffleArray(array) {
  for (let i = array.length - 1; i > 0; i--) {
    // Generate random index
    const j = Math.floor(Math.random() * (i + 1));
    // Swap elements at indices i and j
    [array[i], array[j]] = [array[j], array[i]];
  }
},

    showToast() {
      // Shuffle the messages array before starting the interval
      this.shuffleArray(this.messages);

      const intervalDuration = 22000; // Interval duration in milliseconds

      const intervalId = setInterval(() => {
        // Check if all messages have been shown
        if (this.currentMessageIndex >= this.messages.length) {
          clearInterval(intervalId); // Clear the interval
          return; // Exit the function
        }

        // Show the toast with the current message
        Toastify({
          text: this.messages[this.currentMessageIndex],
          duration: 5000,
          close: true,
          gravity: "bottom",
          position: "left",
          stopOnFocus: true,
          style: {
            background: "linear-gradient(to right, #ffffff, #ffffff)",
            width: "350px",
            padding: "10px",
            color: "#232323"
          },
        }).showToast();

        this.currentMessageIndex++; // Move to the next message
      }, intervalDuration);
    }


    // showToast() {
    //   const intervalDuration = 20000; // Interval duration in milliseconds
    //
    //   const intervalId = setInterval(() => {
    //     // Check if all messages have been shown
    //     if (this.currentMessageIndex >= this.messages.length) {
    //       clearInterval(intervalId); // Clear the interval
    //       return; // Exit the function
    //     }
    //
    //     // Show the toast with the current message
    //     Toastify({
    //       text: this.messages[this.currentMessageIndex],
    //       duration: 5000,
    //       close: true,
    //       gravity: "bottom",
    //       position: "left",
    //       stopOnFocus: true,
    //       style: {
    //         background: "linear-gradient(to right, #ffffff, #ffffff)",
    //         width: "320px",
    //         padding: "10px",
    //         color: "#232323"
    //       },
    //     }).showToast();
    //
    //     this.currentMessageIndex++; // Move to the next message
    //   }, intervalDuration);
    // }
  },

  mounted() {
    this.showToast()
  }
}

</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  cursor: pointer;
  counter-reset: Serial;
  font-family: 'Outfit', sans-serif;
  background: hsla(0, 0%, 100%, 1.0);

  /*background: #f4f5f6;*/
}
a{
  text-decoration: none;
}
input{
  font-family: 'Outfit', sans-serif;
}
textarea{
  font-family: 'Outfit', sans-serif;
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
/* Firefox */
input[type=number] {
  -moz-appearance: textfield;
}
.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}
.route-enter-active {
  transition: all 1s ease-out;
}
.route-leave-to {
  opacity: 0;
  transform: translateX(-100px);
}
.route-leave-active {
  transition: all 1s ease-in;
}

.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: 1s ease all;
}

.mobile-nav-enter-from,
.mobile-nav-leave-to{
  transform: translateX(-250px);
}

.mobile-nav-enter-to{
  transform: translateX(0);
}

.whatsapp_float {
  position: fixed;
  width: 55px;
  height: 55px;
  bottom: 40px;
  right: 40px;
  background-color: #25d366;
  color: #fff;
  border-radius: 50px;
  text-align: center;
  font-size: 30px;
  z-index: 100;
}

.bxl-whatsapp {
  position: absolute;
  top: 21%;
  right: 22.5%;
}

/* for mobile */
@media screen and (max-width: 767px){
  .whatsapp-icon {
    margin-top: 10px;
  }
  .whatsapp_float {
    width: 40px;
    height: 40px;
    bottom: 20px;
    right: 10px;
    font-size: 22px;
  }
}
</style>
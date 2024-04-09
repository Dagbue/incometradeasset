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
        " 🇩🇿 John made a deposit of $5,000",
        " 🇮🇹 Ivan made a deposit of $1,660",
        " 🇪🇸 Evan made a deposit of $750",
        " 🇺🇸 Rachel made a deposit of $300",
        " 🇮🇳 Quinn made a withdrawal of $550",
        " 🇪🇸 Fiona made a deposit of $2,450",
        " 🇨🇳 Ivan made a withdrawal of $1,500",
        " 🇺🇸 Evan made a deposit of $3,450",
        " 🇲🇽 Diana made a withdrawal of $280",
        " 🇲🇽 Quinn made a deposit of $390",
        " 🇿🇦 Bob made a deposit of $1,600",
        " 🇦🇪 Oscar made a deposit of $870",
        " 🇷🇺 Penny made a deposit of $868",
        " 🇩🇪 Evan made a withdrawal of $2,410",
        " 🇷🇺 Fiona made a withdrawal of $485",
        " 🇺🇸 Charlie made a deposit of $1,200",
        " 🇧🇷 Charlie made a withdrawal of $458",
        " 🇨🇦 Steve made a withdrawal of $310",
        " 🇸🇬 Steve made a withdrawal of $2,170",
        " 🇦🇪 Linda made a deposit of $305",
        " 🇦🇪 Steve made a deposit of $230",
        " 🇦🇪 Evan made a withdrawal of $1,540",
        " 🇰🇷 Ivan made a withdrawal of $139",
        " 🇯🇵 Evan made a deposit of $640",
        " 🇸🇬 Linda made a withdrawal of $140",
        " 🇺🇸 Rachel made a withdrawal of $319",
        " 🇷🇺 Oscar made a withdrawal of $106",
        " 🇳🇿 Julia made a deposit of $2,064",
        " 🇬🇧 Steve made a withdrawal of $430",
        " 🇬🇧 Penny made a deposit of $189",
        " 🇫🇷 Mike made a withdrawal of $920",
        " 🇯🇵 Hannah made a deposit of $299",
        " 🇨🇳 Ivan made a deposit of $4,530",
        " 🇮🇹 Steve made a deposit of $468",
        " 🇨🇦 Charlie made a deposit of $1,590",
        " 🇦🇪 George made a deposit of $2,160",
        " 🇪🇸 George made a withdrawal of $451",
        " 🇨🇦 Fiona made a withdrawal of $6,470",
        " 🇦🇪 Steve made a withdrawal of $320",
        " 🇮🇳 Bob made a deposit of $340",
        " 🇷🇺 Ivan made a deposit of $3,000",
        " 🇸🇬 Alice made a withdrawal of $327",
        " 🇧🇷 Oscar made a deposit of $2,360",
        " 🇦🇺 Quinn made a deposit of $1,560",
        " 🇸🇦 Steve made a deposit of $470",
        " 🇫🇷 Ivan made a deposit of $1,690",
        " 🇫🇷 Steve made a withdrawal of $3,340",
        " 🇿🇦 Hannah made a deposit of $610",
        " 🇲🇽 Linda made a deposit of $4,470",
        " 🇧🇷 Nora made a withdrawal of $4,060",
        " 🇰🇷 Nora made a withdrawal of $2,620",
        " 🇦🇪 Fiona made a withdrawal of $230",
        " 🇦🇪 Hannah made a deposit of $1,040",
        " 🇸🇬 Steve made a deposit of $380",
        " 🇳🇿 Diana made a withdrawal of $2,480",
        " 🇯🇵 Linda made a withdrawal of $570",
        " 🇰🇷 Linda made a withdrawal of $540",
        " 🇮🇹 Linda made a withdrawal of $1,250",
        " 🇫🇷 George made a deposit of $2,970",
        " 🇨🇳 Rachel made a deposit of $1,430",
        " 🇨🇦 Bob made a withdrawal of $4,940",
        " 🇩🇪 George made a withdrawal of $1,550",
        " 🇩🇿 Alex made a deposit of $50,000",
        " 🇮🇹 Maria made a deposit of $166,000",
        " 🇪🇸 Lucas made a deposit of $750,000",
        " 🇺🇸 Emma made a deposit of $300,000",
        " 🇮🇳 Aryan made a withdrawal of $550,000",
        " 🇪🇸 Sofia made a deposit of $2,450,000",
        " 🇨🇳 Leo made a withdrawal of $1,000,000",
        " 🇲🇽 Diego made a withdrawal of $280,000",
        " 🇲🇽 Isabella made a deposit of $390,000",
        " 🇿🇦 Ethan made a deposit of $900,000",
        " 🇦🇪 Noah made a deposit of $870,000",
        " 🇷🇺 Olivia made a deposit of $868,000",
        " 🇩🇪 Daniel made a withdrawal of $410,000",
        " 🇷🇺 Ava made a withdrawal of $485,000",
        " 🇺🇸 William made a deposit of $1,000,000",
        " 🇧🇷 James made a withdrawal of $458,000",
        " 🇨🇦 Harper made a withdrawal of $310,000",
        " 🇸🇬 Benjamin made a withdrawal of $170,000",
        " 🇦🇪 Amelia made a deposit of $305,000",
        " 🇦🇪 Jack made a deposit of $230,000",
        " 🇦🇪 Charlotte made a withdrawal of $540,000",
        " 🇰🇷 Henry made a withdrawal of $139,000",
        " 🇯🇵 Evelyn made a deposit of $640,000",
        " 🇸🇬 Logan made a withdrawal of $140,000",
        " 🇺🇸 Sophia made a withdrawal of $319,000",
        " 🇷🇺 Jacob made a withdrawal of $106,000",
        " 🇳🇿 Mila made a deposit of $964,000",
        " 🇬🇧 Aiden made a withdrawal of $430,000",
        " 🇬🇧 Lily made a deposit of $189,000",
        " 🇫🇷 Joseph made a withdrawal of $920,000",
        " 🇯🇵 Zoe made a deposit of $299,000",
        " 🇨🇳 Owen made a deposit of $530,000",
        " 🇮🇹 Michael made a deposit of $468,000",
        " 🇨🇦 Grace made a deposit of $590,000",
        " 🇦🇪 Ryan made a deposit of $960,000",
        " 🇪🇸 Chloe made a withdrawal of $451,000",
        " 🇨🇦 Nora made a withdrawal of $770,000",
        " 🇦🇪 Luke made a withdrawal of $320,000",
        " 🇮🇳 Adam made a deposit of $340,000",
        " 🇷🇺 Hannah made a deposit of $1,000,000",
        " 🇸🇬 Zoe made a withdrawal of $327,000",
        " 🇧🇷 Eli made a deposit of $860,000",
        " 🇦🇺 Ella made a deposit of $560,000",
        " 🇸🇦 Scarlett made a deposit of $470,000",
        " 🇫🇷 Mason made a deposit of $690,000",
        " 🇫🇷 Carter made a withdrawal of $940,000",
        " 🇿🇦 Riley made a deposit of $610,000",
        " 🇲🇽 Layla made a deposit of $870,000",
        " 🇧🇷 Lillian made a withdrawal of $960,000",
        " 🇰🇷 Madison made a withdrawal of $620,000",
        " 🇦🇪 Aria made a withdrawal of $230,000",
        " 🇦🇪 Penelope made a deposit of $840,000",
        " 🇸🇬 David made a deposit of $380,000",
        " 🇳🇿 Victoria made a withdrawal of $480,000",
        " 🇯🇵 Samuel made a withdrawal of $570,000",
        " 🇰🇷 Josephine made a withdrawal of $540,000",
        " 🇮🇹 Camila made a withdrawal of $850,000",
        " 🇫🇷 Gabriel made a deposit of $970,000",
        " 🇨🇳 Julian made a deposit of $1,000,000",
        " 🇨🇦 Lucas made a withdrawal of $940,000",
        " 🇩🇪 Mateo made a withdrawal of $550,000",
        " 🇩🇿 Alex made a deposit of $50,000",
        " 🇮🇹 Maria made a deposit of $166,000",
        " 🇪🇸 Lucas made a deposit of $750,000",
        " 🇺🇸 Emma made a deposit of $300,000",
        " 🇮🇳 Aryan made a withdrawal of $550,000",
        " 🇪🇸 Sofia made a deposit of $450,000",
        " 🇨🇳 Leo made a withdrawal of $500,000",
        " 🇺🇸 Mia made a deposit of $450,000",
        " 🇲🇽 Diego made a withdrawal of $280,000",
        " 🇲🇽 Isabella made a deposit of $390,000",
        " 🇿🇦 Ethan made a deposit of $600,000",
        " 🇦🇪 Noah made a deposit of $870,000",
        " 🇷🇺 Olivia made a deposit of $868,000",
        " 🇩🇪 Daniel made a withdrawal of $410,000",
        " 🇷🇺 Ava made a withdrawal of $485,000",
        " 🇺🇸 William made a deposit of $200,000",
        " 🇧🇷 James made a withdrawal of $458,000",
        " 🇨🇦 Harper made a withdrawal of $310,000",
        " 🇸🇬 Benjamin made a withdrawal of $170,000",
        " 🇦🇪 Amelia made a deposit of $305,000",
        " 🇦🇪 Jack made a deposit of $230,000",
        " 🇦🇪 Charlotte made a withdrawal of $540,000",
        " 🇰🇷 Henry made a withdrawal of $139,000",
        " 🇯🇵 Evelyn made a deposit of $640,000",
        " 🇸🇬 Logan made a withdrawal of $140,000",
        " 🇺🇸 Sophia made a withdrawal of $319,000",
        " 🇷🇺 Jacob made a withdrawal of $106,000",
        " 🇳🇿 Mila made a deposit of $064,000",
        " 🇬🇧 Aiden made a withdrawal of $430,000",
        " 🇬🇧 Lily made a deposit of $189,000",
        " 🇫🇷 Joseph made a withdrawal of $920,000",
        " 🇯🇵 Zoe made a deposit of $299,000",
        " 🇨🇳 Owen made a deposit of $530,000",
        " 🇮🇹 Michael made a deposit of $468,000",
        " 🇨🇦 Grace made a deposit of $590,000",
        " 🇦🇪 Ryan made a deposit of $160,000",
        " 🇪🇸 Chloe made a withdrawal of $451,000",
        " 🇨🇦 Nora made a withdrawal of $470,000",
        " 🇦🇪 Luke made a withdrawal of $320,000",
        " 🇮🇳 Adam made a deposit of $340,000",
        " 🇷🇺 Hannah made a deposit of $1,000,000",
        " 🇸🇬 Zoe made a withdrawal of $327,000",
        " 🇧🇷 Eli made a deposit of $360,000",
        " 🇦🇺 Ella made a deposit of $560,000",
        " 🇸🇦 Scarlett made a deposit of $470,000",
        " 🇫🇷 Mason made a deposit of $1,000,000",
        " 🇫🇷 Carter made a withdrawal of $340,000",
        " 🇿🇦 Riley made a deposit of $610,000",
        " 🇲🇽 Layla made a deposit of $470,000",
        " 🇧🇷 Lillian made a withdrawal of $60,000",
        " 🇰🇷 Madison made a withdrawal of $620,000",
        " 🇦🇪 Aria made a withdrawal of $230,000",
        " 🇦🇪 Penelope made a deposit of $40,000",
        " 🇸🇬 David made a deposit of $380,000",
        " 🇳🇿 Victoria made a withdrawal of $480,000",
        " 🇯🇵 Samuel made a withdrawal of $570,000",
        " 🇰🇷 Josephine made a withdrawal of $540,000",
        " 🇮🇹 Camila made a withdrawal of $250,000",
        " 🇫🇷 Gabriel made a deposit of $970,000",
        " 🇨🇳 Julian made a deposit of $430,000",
        " 🇨🇦 Lucas made a withdrawal of $940,000",
        " 🇩🇪 Mateo made a withdrawal of $550,000",
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
            // width: "20%",
            color: "#232323",
            borderRadius: "4px"
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
<template>
  <div class="containers">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <div class="carousel">
          <div class="carousel-imgs">
            <img
              src="../../assets/slide/slide-1.jpg"
              class="carousel-img"
              alt=""
            />
          </div>
          <div class="carousel-content">
            <h1 class="carousel-title">Welcome to Sailor</h1>
            <p class="carousel-text">
              Ut velit est quam dolor ad a aliquid qui aliquid. Sequi ea ut et
              est quaerat sequi nihil ut aliquam. Occaecati alias dolorem
              mollitia ut. Similique ea voluptatem. Esse doloremque accusamus
              repellendus deleniti vel. Minus et tempore modi architecto.
            </p>
            <div class="carousel-btns-sc">
              <button class="carousel-btn">Read More</button>
            </div>
          </div>
          <div class="overlow"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="carousel">
          <div class="carousel-imgs">
            <img
              src="../../assets/slide/slide-2.jpg"
              class="carousel-img"
              alt=""
            />
          </div>
          <div class="carousel-content">
            <h1 class="carousel-title">Lorem Ipsum Dolor</h1>
            <p class="carousel-text">
              Ut velit est quam dolor ad a aliquid qui aliquid. Sequi ea ut et
              est quaerat sequi nihil ut aliquam. Occaecati alias dolorem
              mollitia ut. Similique ea voluptatem. Esse doloremque accusamus
              repellendus deleniti vel. Minus et tempore modi architecto.
            </p>
            <div class="carousel-btns-sc">
              <button class="carousel-btn">Read More</button>
            </div>
          </div>
          <div class="overlow"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="carousel">
          <div class="carousel-imgs">
            <img
              src="../../assets/slide/slide-3.jpg"
              class="carousel-img"
              alt=""
            />
          </div>
          <div class="carousel-content">
            <h1 class="carousel-title">Sequi ea ut et est quaerat</h1>
            <p class="carousel-text">
              Ut velit est quam dolor ad a aliquid qui aliquid. Sequi ea ut et
              est quaerat sequi nihil ut aliquam. Occaecati alias dolorem
              mollitia ut. Similique ea voluptatem. Esse doloremque accusamus
              repellendus deleniti vel. Minus et tempore modi architecto.
            </p>
            <div class="carousel-btns-sc">
              <button class="carousel-btn">Read More</button>
            </div>
          </div>
          <div class="overlow"></div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-button-prev prev" slot="button-prev"></div>
      <div class="swiper-button-next next" slot="button-next"></div>
    </swiper>
    <div class="about">
      <div class="about-left">
        <h2 class="about-title">EUM IPSAM LABORUM DELENITI VELITENA</h2>
        <p class="about-text">
          Voluptatem dignissimos provident quasi corporis voluptates sit assum
          perenda sruen jonee trave
        </p>
      </div>
      <div class="about-right">
        <p class="about-content">
          Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
          irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
          fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident,
          sunt in culpa qui officia deserunt mollit anim id est laborum
        </p>
        <ul class="about-list">
          <li class="about-item">
            <i class="fas fa-check-double icon"></i>
            Ullamco laboris nisi ut aliquip ex ea commodo consequa
          </li>
          <li class="about-item">
            <i class="fas fa-check-double icon"></i>
            Duis aute irure dolor in reprehenderit in voluptate velit
          </li>
          <li class="about-item">
            <i class="fas fa-check-double icon"></i>
            Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
            irure dolor in reprehenderit in
          </li>
        </ul>
        <p class="about-item">
          <i>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </i>
        </p>
      </div>
    </div>
    <div class="clients">
      <div class="clients-content">
        <div class="clients-imgs">
          <img src="../../assets/clients/client-1.png" class="clients-circle" />
        </div>
        <div class="clients-imgs">
          <img src="../../assets/clients/client-2.png" class="clients-circle" />
        </div>
        <div class="clients-imgs">
          <img src="../../assets/clients/client-3.png" class="clients-circle" />
        </div>
        <div class="clients-imgs">
          <img src="../../assets/clients/client-4.png" class="clients-circle" />
        </div>
        <div class="clients-imgs">
          <img src="../../assets/clients/client-5.png" class="clients-circle" />
        </div>
        <div class="clients-imgs">
          <img src="../../assets/clients/client-6.png" class="clients-circle" />
        </div>
      </div>
    </div>
    <transition name="back-to-top-fade">
      <div class="backtotop" v-show="visible" @click="backtotop">
        <button class="btn-top"><i class="fa fa-chevron-up"></i></button>
      </div>
    </transition>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
export default {
  data() {
    return {
      swiperOption: {
        slidesPerView: 1,
        spaceBetween: 1,
        loop: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
      visibleoffset: 150,
      visible: false,
    };
  },
  name: "HomeComponent",
  components: {
    Swiper,
    SwiperSlide,
  },
  mounted() {
    window.smoothScroll = () => {
      let currentScroll =
        document.documentElement.scrollTop || document.body.scrollTop;
      if (currentScroll > 0) {
        window.requestAnimationFrame(window.smoothScroll);
        window.scrollTo(0, Math.floor(currentScroll - currentScroll / 5));
      }
    };
    window.addEventListener("scroll", this.catchScroll);
  },
  destroy() {
    window.removeEventListener("scroll", this.catchScroll);
  },
  methods: {
    catchScroll() {
      this.visible = window.pageYOffset > parseInt(this.visibleoffset);
    },
    backtotop() {
      window.smoothScroll();
      // this.$emit("scrolled");
    },
  },
};
</script>
<style lang="scss" scoped>
.carousel {
  width: 100vw;
  height: 100vh;
  position: relative;
  // overflow: hidden;
  &-imgs {
    width: 100%;
    height: 100%;
  }
  &-img {
    width: -webkit-fill-available;
    height: -webkit-fill-available;
  }
  &-content {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
  &-title {
    position: relative;
    margin-top: 215px;
    text-align: center;
    font-family: "Raleway", sans-serif;
    font-weight: 700;
    font-size: 48px;
    color: #fff;
    z-index: 1;
  }
  &-text {
    position: relative;
    text-align: center;
    padding: 25px 228px 0;
    font-family: "Raleway", sans-serif;
    color: #fff;
    font-size: 17px;
    z-index: 1;
  }
  &-btns-sc {
    position: relative;
    z-index: 1;
    text-align: center;
    padding-top: 25px;
  }
  &-btn {
    width: 125px;
    height: 34px;
    border: none;
    background: #d9232d;
    color: #fff;
    font-size: 13px;
    font-family: "Raleway";
    font-weight: 600;
    border-radius: 5px;
    cursor: pointer;
    &:hover {
      opacity: 0.9;
    }
  }
}

.overlow {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: #000;
  opacity: 0.5;
}

.next,
.prev {
  width: 50px;
  height: 50px;
  color: #d9232d;
  background: #fff9;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 44px;
  border-radius: 50%;
  cursor: pointer;
  position: absolute;
  z-index: 3;
}
.prev {
  margin-left: 44px;
}

.swiper-button-prev:after,
.swiper-button-next:after {
  font-size: 21px;
  font-weight: 900;
}
.about {
  display: flex;
  padding: 60px 0;
  margin: 0 113px;
  &-left,
  &-right {
    width: 636px;
  }

  &-title {
    font-family: "Raleway";
    font-size: 48px;
    font-weight: 700;
    margin-bottom: 20px;
    opacity: 0.7;
  }
  &-text {
    font-size: 27px;
    font-family: "Raleway";
  }
  &-content {
    font-family: "Poppins";
    font-weight: 300;
    margin-bottom: 24px;
  }
  &-list {
    list-style: none;
  }
  &-item {
    font-family: "Raleway";
    padding: 6px 0px;
  }
}
.icon {
  font-size: 12px;
  color: #d9232d;
  padding-right: 6px;
}
.clients {
  padding: 15px 0;
  background: #f8f9fa;
  &-content {
    margin: 0px 100px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &-imgs {
    width: 219px;
    height: 78px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &-circle {
    max-width: 45%;
    transition: all 0.4s ease-in-out;
    display: inline-block;
    padding: 15px 0;
    filter: grayscale(100);
    cursor: pointer;
    &:hover {
      filter: none;
      transform: scale(1.15);
    }
  }
}
.back-to-top-fade-enter-active,
.back-to-top-fade-leave-active {
  transition: opacity 0.5s;
}
.back-to-top-fade-enter,
.back-to-top-fade-leave-to {
  opacity: 0;
}
.backtotop {
  position: fixed;
  right: 30px;
  width: 50px;
  height: 25px;
  bottom: 50px;
  z-index: 99999;
}
.btn-top {
  border: none;
  width: 50px;
  height: 50px;
  font-size: 23px;
  border-radius: 50%;
}
</style>

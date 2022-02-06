<template>
  <div class="header">
    <h1 class="header__logo">
      <router-link tag="a" to="/" class="header__link">SAILOR</router-link>
    </h1>
    <div class="menu">
      <ul class="menu__item">
        <li class="menu__chill">
          <router-link tag="a" to="/" class="menu__link">Home</router-link>
        </li>
        <li class="menu__chill">
          <router-link tag="a" to="/views/about/index" class="menu__link"
            >About <i class="fa fa-angle-down"></i
          ></router-link>
          <ul class="sub__menu">
            <li class="sub__item">
              <router-link tag="a" to="/views/home/Home.vue" class="menu__link"
                >About
              </router-link>
            </li>
            <li class="sub__item">
              <router-link tag="a" to="/views/home/Home.vue" class="menu__link"
                >Team
              </router-link>
            </li>
            <li class="sub__item">
              <router-link tag="a" to="/views/home/Home.vue" class="menu__link"
                >Testimonials
              </router-link>
            </li>
            <li class="sub__item">
              <router-link tag="a" to="/views/home/Home.vue" class="menu__link"
                >Deep Drop Down
              </router-link>
            </li>
          </ul>
        </li>
        <li class="menu__chill">
          <router-link tag="a" to="/views/services/Services" class="menu__link"
            >Services</router-link
          >
        </li>
        <li class="menu__chill">
          <router-link
            tag="a"
            to="/views/portfolio/Portfolio"
            class="menu__link"
            >Portfolio</router-link
          >
        </li>
        <li class="menu__chill">
          <router-link tag="a" to="/views/pricing/Pricing" class="menu__link"
            >Pricing</router-link
          >
        </li>
        <li class="menu__chill">
          <router-link tag="a" to="/views/blog/Blog" class="menu__link"
            >Blog</router-link
          >
        </li>
        <li class="menu__chill">
          <router-link
            tag="a"
            to="/views/contact/Contact.vue"
            class="menu__link"
            >Contact</router-link
          >
        </li>
        <li class="menu__chill">
          <router-link tag="a" to="/" class="menu__btn"
            >Get Started</router-link
          >
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  margin: 0px 98px;
  padding: 0 15px;
  position: relative;
  z-index: 2;
  &__logo {
    margin: 0;
    margin-right: 443px;

    .header__link {
      color: #556270;
      font-family: "Poppins", sans-serif;
      text-decoration: none;
      font-weight: 700;
      text-transform: uppercase;
      font-size: 28px;
    }
  }
}

.menu__item {
  display: flex;

  .menu__chill {
    list-style: none;
    position: relative;
    .menu__link {
      font-family: "Poppins", sans-serif;
      color: #556270;
      text-decoration: none;
      padding: 10px 0px 11px 26px;

      &:hover {
        color: #d9232d;
      }
    }
    &:hover .sub__menu {
      top: 25px;
      opacity: 1;
      visibility: visible;
    }

    .menu__btn {
      color: #fff;
      padding: 8px 25px;
      margin-left: 30px;
      text-decoration: none;
      border-radius: 5px;
      font-weight: 600;
      background-color: #d9232d;
      font-family: "Poppins", sans-serif;
      transition: linear 0.5s;

      &:hover {
        opacity: 0.8;
      }
    }
  }
  .sub__menu {
    list-style: none;
    position: absolute;
    top: 35px;
    background-color: #fff;
    box-shadow: 0px 0px 30px rgb(127 137 161 / 25%);
    width: 176px;
    margin-left: 17px;
    line-height: 39px;
    opacity: 0;
    visibility: hidden;
    transition: linear 0.3s;
  }
}
</style>

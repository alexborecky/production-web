<template>
  <div class="burger-nav flex center">
      <div class="open">
          <div class="flex middle" @click="isActive = !isActive" >
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M3 12H21M3 6H21M3 18H21" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
          </div> 
      </div>
    <transition name="fade">
      <div class="nav-container flex center-column-top" :class="{ passive: isActive }">
          <div class="container flex center-column-right">
            <div class="top-bar flex full-width">
              <div class="logo flex center" @click="isActive = !isActive">
                <nuxt-link to="/" class="logo">Alex Borecky</nuxt-link>
              </div>
              <div class="close flex">
                  <div class="flex middle" @click="isActive = !isActive" >
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M18 6L6 18M6 6L18 18" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                  </div> 
              </div>
            </div>
            <div class="mobile-links flex center-column-top">
                <ul>
                    <li @click="isActive = !isActive"><nuxt-link to="/">Work</nuxt-link></li>
                    <li @click="isActive = !isActive"><nuxt-link to="/About">About</nuxt-link></li>
                    <li @click="isActive = !isActive"><nuxt-link to="/Contact">Contact</nuxt-link></li>
                </ul>
            </div>
          </div>
      </div> 
    </transition>
  </div>
</template>

<script>


export default {
  name: 'sideBar',
  data () {
    return {
      isActive: true
    }
  },
  methods: {
  }
}
</script>



<style lang="scss">

.fade-enter-active, .fade-leave-active {
transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
opacity: 1;
}

.passive {
opacity: 0;
z-index: -1000;
height: 0vh;
transform: translateX(100%) !important;
position: absolute;
}

.open {
  width: 100%;
  height: 100%;
  float: right;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  svg {
    transition: .3s ease-in-out;
    rect {
      transition: .3s ease-in-out;
      fill: rgba($color: white, $alpha: 0);
    }
  }
  &:hover {
    cursor: pointer;
    svg {
      rect {
        fill: rgba($color: white, $alpha: .4);
        stroke: black;
        &:nth-child(1) {
          width: 32px;
        }
        &:nth-child(2) {
          width: 32px;
          transform: translateX(6px);
        }
        &:nth-child(3) {
          width: 24px;
        }
      }
    }
  }
  @media (max-width:680px) {
    svg {
      width: 32px;
    }
  }
}


.burger-nav {
z-index: 100;
width: auto;
.nav-container {
  position: fixed;
  top: 0 !important;
  left: 100%;
  width: 100% !important;
  height: 100vh;
  background-color: black;
  z-index: 100;
  transition: .4s ease-in;
  transform: translateX(-100%);
  .container {
    position: relative;
    height: 100%;
    .top-bar {
      position: absolute;
      height: 80px !important;
      justify-content: space-between;
      align-items: center;
      a {
        color: white;
        &:hover {
          opacity: 0.4 !important;
          color: white !important;
        }
      }
    }
    .close {
      z-index: 1005;
      background-color: black;
      height: 56px;
      width: 40px;
      justify-content: flex-end;
      align-items: center;
      svg {
        transition: .3s ease-in-out;
        rect {
          transition: .3s ease-in-out;
        }
      }
      &:hover {
        cursor: pointer;
        svg {
          rect {
            fill: rgba($color: black, $alpha: 1);
            stroke: white;
          }
        }
      }
    }
  }
}
}


.mobile-links {
display: flex; 
justify-content: center;
text-align: center;
height: 100%;
padding: 0;
text-align: center;
margin-top: 40px;
width: 100%;
.logo {
    img {
        max-width: 280px;
        @media only screen and (max-width: 560px) {
          height: 24px;
        }
      }
  }
  ul {
      margin-top: -120px;
      padding-left: 0;
      list-style-type: none;
  a {
    color: white;
    margin: 20px 0;
    display: flex;
    justify-content: center;
    text-decoration: none;
    font-size: 24px;
    @media (max-width: 680px) {
      font-size: 24px;
    }
    &:hover {
      color: white !important;
    }
  }
}
}


.nuxt-link-exact-active {
color: white ;
}


@media only screen and (min-width: 720px) {
    .burger-nav {
        display: none;
    }
}

.logo {
  font-family: "area-extended", sans-serif;
  font-weight: 700;
  font-size: 14px;
  font-style: normal;
  color: white;
  text-decoration: none;
}

</style>

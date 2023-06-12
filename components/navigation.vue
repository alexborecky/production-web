<template>
    <div class="navigation flex center full-width navbar" :class="{ 'hidden-navbar': !showNavbar, scrolled: !scrolledNav}">
        <div class="container flex">
            <nuxt-link to="/" class="logo"> 
                <!-- <img src="@/assets/images/logo.svg" alt="Shopteťák.cz logo"> -->
                Alex Borecky
            </nuxt-link>
            <div class="links flex middle">
                <ul class="flex center">
                    <li><nuxt-link to="/">Work</nuxt-link></li>
                    <li><nuxt-link to="/about">About</nuxt-link></li>
                    <li><nuxt-link to="/contact">Contact</nuxt-link></li>
                </ul>
            </div>
            <sideBar/>
        </div>
    </div>
</template>


<script>
const OFFSET = 60
export default {
    name: 'navigation',
    data () {
    return {
      showNavbar: true,
      scrolledNav: true,
      lastScrollPosition: 0,
      scrollValue: 0
    }
  },

  mounted () {
    this.lastScrollPosition = window.pageYOffset
    window.addEventListener('scroll', this.onScroll)
    const viewportMeta = document.createElement('meta')
    viewportMeta.name = 'viewport'
    viewportMeta.content = 'width=device-width, initial-scale=1'
    document.head.appendChild(viewportMeta)
  },

  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },

  methods: {
    onScroll () {
      if (window.pageYOffset < 0) {
        return
      }
      if (Math.abs(window.pageYOffset - this.lastScrollPosition) < OFFSET) {
        return 
      }
      this.showNavbar = window.pageYOffset < this.lastScrollPosition
      this.scrolledNav = window.pageYOffset < this.lastScrollPosition
      this.lastScrollPosition = window.pageYOffset
    }
  }
}


</script>


<style lang="scss" scoped>

.navigation {
    height: 100px;
    background-color: rgba($color: #181818, $alpha: .88);
    backdrop-filter: blur(16px);
    position: sticky;
    top: 0;
    z-index: 1000;
    justify-content: center;
    transition: 0.2s all ease-out;
    
    @media only screen and (max-width: 720px) {
        height: 80px;
        position: fixed !important;
        margin-top: 0;
        .links {
            display: none;  
        }
        .container {
            .logo {
                font-family: "area-extended", sans-serif;
                font-weight: 700;
                font-size: 14px;
                font-style: normal;
            }
        }
    }
    .container {
        height: 40px;
        align-items: center;
        justify-content: space-between;
        .logo {
            font-family: "area-extended", sans-serif;
                font-weight: 700;
                font-size: 14px;
                font-style: normal;
                color: white;
                text-decoration: none;
        }
        ul {
            padding-left: 0;
            list-style: none;
            li {
                margin-left: 80px;
                @media only screen and (max-width: 1600px) {
                    margin-left: 40px;
                }
                a {
                    font-size: 14px;
                    letter-spacing: -1.16%;
                    text-decoration: none;
                }
            }
        }
    }
}

.nuxt-link-exact-active {
    color: #E3FF34;
}

.navigation.hidden-navbar {
  box-shadow: none;
  transform: translate3d(0, -120%, 0);
}

.scrolled {
        background-color: #181818 !important;
    }

</style>
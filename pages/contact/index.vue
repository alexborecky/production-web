<template>
    <div class="main-container contact">
        <div class="main-container flex flex-center">
            <div class="container flex column">
                <h1>Get in touch!</h1>
                <ul class="flex">
                    <li class="flex center"><a href="https://calendly.com/boreckyalex/chat-with-alex" target="_blank">Book a meeting</a>
                        <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M8 24L23.5 8.5" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                            <path d="M11 8H24V21" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                        </svg>
                    </li>
                    <li class="flex center"><a href="mailto:boreckyalex@gmail.com" target="_blank">Email</a>
                        <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M8 24L23.5 8.5" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                            <path d="M11 8H24V21" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                        </svg>
                    </li>
                    <li class="flex center"><a href="https://www.instagram.com/alex.borecky/" target="_blank">Instagram</a>
                        <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M8 24L23.5 8.5" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                            <path d="M11 8H24V21" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                        </svg>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import externalButton from '../../components/externalButton.vue'
    export default {
  components: { externalButton },
        
    }
</script>

<style lang="scss" scoped>

ul {
    margin-top: 80px;
    padding-left: 0px;
    text-align: left;
    list-style: none;
    li {
        text-decoration: none;
        margin-bottom: 8px;
        margin-right: 64px;
        a {
            text-decoration: none;
            font-size: 24px;
            line-height: 40px;
            letter-spacing: -1.12%;
        }
        svg {
            margin-left: 8px;
            transition: ease-in-out .2s; 
            path {
                transition: ease-in-out .2s;
            }
        }
        &:hover {
            svg {
                path {
                    stroke:#E3FF34;
                }
                transform: translate(4px ,-4px);
            }
        }
    }
    @media (max-width: 960px) {
        flex-flow: column;
    }
}

h1 {
    @media (max-width: 600px) {
        font-size: 40px;
        line-height: 52px;
        letter-spacing: -1.16%;
    }
}

</style>
<template>
    <div class="main-container">
        <div class="flex column center">
            <div class="container flex column center-column-left">
                <div class="message">
                    <h1>Oops... We're working on it!</h1>
                    <p>The page is currently being coded and is currently unavailable.</p>
                </div>
                <!-- <div class="trailer-message">
                    <h2> You can <a href="https://youtu.be/xLExJm6A13A" target="_blank">watch the film</a> in the meantime! </h2>
                </div> -->
                <nuxt-link to="/" class="back-home flex center">
                    <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M27 16H5" stroke="white" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M14 7L5 16L14 25" stroke="white" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    Back home 
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
    export default {

    }
</script>

<style lang="scss" scoped>

.message {
    text-align: left;
    p {
        margin-top: 20px;
    }
}

.trailer-message {
    margin-top: 80px;
    h2 {
        text-align: left;
    }
    a {
        text-decoration: underline;
    }
}

.back-home {
    margin-top: 80px;
            text-decoration: none;
            font-size: 24px;
            line-height: 40px;
            letter-spacing: -1.12%;
        svg {
            margin-right: 8px;
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
                transform: translate(-4px , 0px);
            }
        }
    }

</style>
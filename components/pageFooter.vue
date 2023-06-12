<template>
    <div class="footer full-width flex">
        <div class="footer-column column-one flex">
            <h2>Get in touch</h2>
        </div>  
        <div class="footer-column column-two flex">
            <ul class="flex column">
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
</template>

<script>
    export default {
        name: 'pageFooter'
    }
</script>

<style lang="scss" scoped>

.footer {
    justify-content: space-evenly;
    height: 240px;
    margin-bottom: 56px;
    .footer-column {
        width: 100%;
        justify-content: flex-start;
        align-items: flex-start;
    }
    ul {
        text-align: left;
        list-style: none;
        li {
            text-decoration: none;
            margin-bottom: 8px;
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
    }
    h2 {
        font-size: 56px;
        line-height: 56px;
        @media (max-width: 960px) {
        font-size: 40px;
        line-height: 52px;
        letter-spacing: -1.16%;
        }
    }
    @media (max-width: 720px) {
        flex-flow: column;
        .column-two {
            margin-top: 40px;
        }
        ul {
            padding-left: 0px;
        }
    }
}

</style>
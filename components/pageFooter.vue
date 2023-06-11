<template>
    <div class="footer full-width flex">
        <div class="footer-column column-one flex">
            <h2>Get in touch</h2>
        </div>  
        <div class="footer-column column-two flex">
            <ul class="flex column">
                <li><a href="#">Book a meeting</a></li>
                <li><a href="#">Email</a></li>
                <li><a href="#">Instagram</a></li>
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
        }
    }
    h2 {
        font-size: 56px;
        line-height: 56px;
    }
}

</style>
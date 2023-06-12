<template>
    <div class="main-container">
        <div class="flex column center">
            <div class="container flex column">
                <div class="row flex">
                    <div class="image-container">
                        <div class="image"></div>
                    </div>
                    <div class="bio flex center-column-left">
                        <h1>Alexandr Borecký</h1>
                        <p>An award winning director, actor and screenwriter Alexandr Borecky, based in Prague is starting to make his way to the industry despite his family's non-artistic background. His debut as a director and producer can be seen in his short film Origin (2021) , with which he has won several awards and now follows up with another project Untold Pieces (2023) which is being recognized by festivals all around the world.</p>
                        <a href="https://www.imdb.com/name/nm8879254/?ref_=tt_ov_wr" target="_blank" class="flex center">
                            Read more
                            <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M8 24L23.5 8.5" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                                <path d="M11 8H24V21" stroke="#EDEDED" stroke-linecap="square" stroke-linejoin="round"/>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

.container {
    margin-top: 160px;
    .row {
        .image-container {
            width: 100%;
            .image {
                width: 480px;
                height: 640px;
                background-color: red;
                background-image: url(https://ik.imagekit.io/alexborecky/FILM_WEB/DSCF7824-min_D9h-mBREe.jpg?updatedAt=1686564200618);
                background-size: cover;
                background-position: center;
                @media (max-width: 1280px) {
                    width: 320px;
                    height: 440px;
                }
                @media (max-width: 960px) {
                    width: 320px;
                }
                @media (max-width: 720px) {
                    width: 500px;
                }
                @media (max-width: 600px) {
                    width: 400px;
                }
                @media (max-width: 450px) {
                    width: 340px;
                }
            }
        }
        .bio {
            width: 100%;
            h1, p {
                text-align: left;
            }
            h1 {
                @media (max-width: 1280px) {
                    margin-top: 0px;
                }
                @media (max-width: 1280px) {
                    margin-top: 80px;
                }
            }
            p {
                margin-top: 40px;
                margin-bottom: 80px;
            }
            a {
                text-decoration: none;
                font-size: 24px;
                line-height: 40px;
                letter-spacing: -1.12%;
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
        @media (max-width: 960px) {
            flex-flow: column;
        }
    }

@media (max-width: 960px) {
    margin-top: 40px;
}

}

</style>
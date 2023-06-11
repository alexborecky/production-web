<template>
    <div class="main-container contact">
        <div class="full hero flex flex-center">
            <div class="container flex column">
                <h1>Get in touch!</h1>
                <ul>
                    <li><external-button
                        text="Instagram"
                        linkTo="https://instagram.com/alex.borecky"
                        />
                    </li>
                    <li><external-button
                        text="Email"
                        linkTo="mailto:boreckyalex@gmail.com"
                        />
                    </li>
                    <li><external-button
                        text="IMDb"
                        linkTo="https://www.imdb.com/name/nm8879254/?ref_=ext_shr_lnk"
                        />
                    </li>
                </ul>   
                <div class="bio flex">
                    <h2>Bio</h2>
                    <external-button
                    text="Read"
                    linkTo="https://www.imdb.com/name/nm8879254/bio?ref_=nm_ov_bio_sm"
                    />
                </div>             
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

.contact {
    .hero {
        background-image: url(~/assets/images/Contact.jpg);
        background-size: cover;
        @media (max-width: 500px) {
            background-size: auto 100%;
            background-position: 60% 100%;
        }
        .container {
            align-items: flex-start;
            h1 {
                font-size: 80px;
                font-weight: 300;
            }
            ul {
                margin: 40px 0;
                padding-left: 0 !important;
                list-style: none;
                li {
                    margin: 8px 0;
                }
            }
            h2 {
                font-size: 40px;
                margin-right: 24px;
                margin-bottom: 0 !important;
            }
            .bio {
                align-items: flex-end;
                .text-button {
                    margin-bottom: 4px;
                }
            }
        }
    }
}

</style>
<template>
    <div class="socials">
            <div class="row">
                <div class="col-8">
                   <p>COPYRIGHTS 2012 - 2015 AVADA THEME BY AVADA FUSION | ALLRIGHTS RESERVED | POWERED BY WORDPRESS</p>
                </div>
                <div class="col-4">
                    <div class="row">
                        <div class="col icon-container" v-for="(logo, index) in logos" :key="index">
                            <font-awesome-icon :icon="logo.icon" class="icons"/>
                        </div>
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
export default {
    name: 'SocialsComponent',
    data() {
        return {
            logos: [
                {
                    icon: 'fa-brands fa-facebook-f' 
                },
                {
                    icon: 'fa-brands fa-twitter' 
                },
                {
                    icon: 'fa-brands fa-youtube' 
                },
                {
                    icon: 'fa-brands fa-instagram' 
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

.socials{
    background-color: black;
    height: 50px;
    color: $white-color;
    .row{
        height: 100%;
        .col-8, .col-4{
            border: 1px solid $white-color;
            height: 80%;
        }
        .col-4{
            .row{
                display: flex;
                justify-content: flex-end;
                .icon-container{
                    display: flex;
                    flex-direction: column;
                    
                    max-width: fit-content;
                }

            }
        }
    }
}
</style>
<template>
    <div class="socials">
            <div class="row">
                <div class="col-10 text-container">                  
                   <p>COPYRIGHTS 2012 - 2015 AVADA THEME BY AVADA FUSION | ALLRIGHTS RESERVED | POWERED BY WORDPRESS</p>
                </div>
                <div class="col-2">
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
        .col-10, .col-2{
            height: 80%;
        }
        .col-2{
            .row{
                display: flex;
                margin: 0!important;
                .icon-container{
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    margin: 0;
                    padding: 0;            
                    .icons{
                        max-height: 100%;
                        max-width: 100%;
                        font-size: 14px;
                        color: $dove-grey-color;
                    }
                }
            }
        }
        .text-container{
            display: flex;
            align-items: center;
            p{
                margin: 0!important;
                font-size: 10px;
                color: $dove-grey-color;
            }
        }
    }
}
</style>
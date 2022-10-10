<template>
    <div class="tweet">
        <div class="row">
            <div class="col-2 logo-container">
                <!-- <img src="@/assets/img/3a74ce3d0532b7773b174c45ca3bd05a_normal.png" alt=""> -->
                <img :src="`./assets/img/${profileImage}`" :alt="userName">
            </div>
            <div class="col-10 content-container">
                <div class="row">
                    <div class="col user-container">
                        <p> {{ userName }} </p>
                        <p>@{{ userName }}</p>
                    </div>
                    <div class="col twitter-logo-container">
                        <img src="@/assets/img/image (1).svg" alt="">
                    </div>
                </div>
                <div class="row">
                    <div class="col text-container">
                        <p> {{ tweetContent }} </p>
                    </div>
                </div>
                <div class="row">
                    <div class="col image-container">
                        <img src="@/assets/img/En2TRxLW4AEiWUN.jpeg" alt="">
                    </div>
                </div>
                <div class="row">
                    <div class="col-4 action-panel">
                        <font-awesome-icon icon="fa-regular fa-heart" class="icons"/>
                        <font-awesome-icon icon="fa-regular fa-share-from-square" class="icons"/>
                    </div>
                    <div class="col-8 time">
                        <p> {{ postTime }}h</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TweetComponent',
    props: {
        profileImage: String,
        userName: String,
        postTime: Number,
        tweetContent: String
    }
}
</script>

<style scoped lang="scss">
    .tweet{
        p{
            padding: 0!important;
            margin: 0!important;
        }
        .row{
            .logo-container{
                height: 25px;
                img{
                    height: 100%;
                    border-radius: 50%;
                    // width: 100%;
                }
            }
            .col-2,.col-10, .col{
                // border: 1px solid red;
                
                
            }
            .content-container{
                .row{
                    flex-wrap: nowrap!important;

                    .user-container{
                        height: fit-content;
                        p{
                            font-size: 12px;
                        }
                        p:last-child{
                            color: #bcbcbc;
                        }
                    }
                    .twitter-logo-container{
                        height: 20px;
                        display: flex;
                        flex-direction: column;
                        align-items: flex-end;
                        img{
                            height: 100%;
                        }
                    }
                    .text-container{
                        p{
                            font-size: 12px;
                        }
                    }
                    .image-container{
                        width: 100%;
                        img{
                            width: 100%;
                        }
                    }
                    .action-panel{
                        padding: 10px 0;
                        display: flex;
                        flex-direction: row;
                        justify-content: space-between;
                        color: #6b6868;
                    }
                    .time{
                        padding: 10px 0;
                        display: flex;
                        flex-direction: row;
                        justify-content: flex-end;
                        font-size: 12px;
                        color: #6b6868

                    }
                }
                }
            
        }
    }
</style>
<template>
    <div class="announcement">
        <div class="announcement-content">
            <div class="colse" @click="$emit('closeAnnouncement')">
            </div>
            <p class="sub-title">{{$t("marketPlace.a-text0")}}</p>
            <p class="sub-title">{{$t("marketPlace.a-text1")}}。</p>
            <h1>{{$t("marketPlace.a-text2")}}</h1>
            <h2>{{$t("marketPlace.a-text3")}}</h2>
            <p>{{$t("marketPlace.a-text4")}}</p>
            <p>{{$t("marketPlace.a-text5")}}</p>
            <p>{{$t("marketPlace.a-text6")}}</p>
            <p>{{$t("marketPlace.a-text7")}}</p>
            <p>{{$t("marketPlace.a-text8")}}</p>
            <p>{{$t("marketPlace.a-text9")}}</p>
            <div class="list">
                <ul>
                    <li>{{$t("marketPlace.a-text10")}}</li>
                    <li>{{$t("marketPlace.a-text11")}}</li>
                    <li>{{$t("marketPlace.a-text13")}}</li>
                    <li>{{$t("marketPlace.a-text16")}}</li>
                </ul>
            </div>
            <h2>{{$t("marketPlace.a-text17")}}</h2>
            <p>{{$t("marketPlace.a-text18")}}</p>
            <p>{{$t("marketPlace.a-text19")}}</p>
            <p>{{$t("marketPlace.a-text20")}}</p>

            <p>{{$t("marketPlace.a-text21")}}</p>
            <p>{{$t("marketPlace.a-text22")}}</p>
            <h2>{{$t("marketPlace.a-text23")}}</h2>
            <div class="contact">
                <p>{{$t("marketPlace.a-text24")}}</p>
                <p>{{$t("marketPlace.a-text25")}}</p>
                <p>{{$t("marketPlace.a-text26")}}</p>
                <p>{{$t("marketPlace.a-text27")}}</p>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="less">
@imgPath: "../../../assets/img";
    .announcement{
        position: fixed;
        width:100%;
        box-sizing: border-box;
        background: rgba(0, 0, 0, .5);
        z-index: 999;
        top:0px;
        right:0px;
        bottom:0px;
        left:0px;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow-y: auto;
        .announcement-content{
            min-width: 800px;
            padding:20px 60px;
            height: auto;
            background: #fff;
            border-radius: 10px;
            position:relative;
            .colse{
                position:absolute;
                top:20px;
                right:20px;
                width:20px;
                height: 20px;
                background:  url( '@{imgPath}/colse_2.png') center  no-repeat;
                background-size: 100%;
                cursor: pointer;
            }
            h1{
                font-size: 24px;
                font-weight: 300;
                margin-top:20px;
            }
            h2{
                font-size: 18px;
                margin-top:20px;
                margin-bottom: 10px;
            }
            p{
                font-size: 14px;
                margin-bottom: 6px;
            }
            .sub-title{
                font-size: 16px;
                margin-bottom: 0px;
            }
            .list{
                padding-left:40px;
            }
            ul>li{
                list-style: disc;
                font-size: 12px;
            }
            .contact{
                display: flex;
                p{
                    margin-left:20px;
                    margin-bottom: 0;
                }
            }
        }
    }
    @media only screen and (max-width: 720px) {
     
        .announcement{
        position: fixed;
        width:100%;
        background: rgba(0, 0, 0, .5);
        z-index: 999;
        top:0px;
        right:0px;
        left:0px; 
        bottom: 0px;
        display: block;
        .announcement-content{
            width:100%;
            min-width: 100%;
            padding:15px;
            background: #fff;
            border-radius: 0px;
            position: relative;
            top:0;
            .colse{
                position:absolute;
                top:20px;
                right:20px;
                width:20px;
                height: 20px;
                background:  url( '@{imgPath}/colse_2.png') center  no-repeat;
                background-size: 100%;
                cursor: pointer;
            }
            h1{
                font-size: 24px;
                font-weight: 300;
                margin-top:20px;
            }
            h2{
                font-size: 18px;
                margin-top:20px;
                margin-bottom: 10px;
            }
            p{
                font-size: 14px;
                margin-bottom: 6px;
            }
            .sub-title{
                font-size: 16px;
                margin-bottom: 0px;
            }
            .list{
                padding-left:40px;
            }
            ul>li{
                list-style: disc;
                font-size: 12px;
            }
            .contact{
                display: flex;
                flex-wrap: wrap;
                p{
                    margin-left:20px;
                    margin-bottom: 0;
                }
            }
        }
    }
    }
</style>
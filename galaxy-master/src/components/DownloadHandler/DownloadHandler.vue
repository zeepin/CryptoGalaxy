<template>
  <div  >
    <div class="page" v-if="isHlep">
    <div class="hd">
      <img class="logo" src="@/assets/img/download_logo.png" alt="" />
      <div class="title">CryptoGalaxy</div>
      <div class="version">2.1.5</div>
      <div class="des">Discover &amp; Collect Your Planet </div>
      <div class="subdes">The first ever virtual universe based on blockchain</div>
    </div>

  <!--   <div class="bd">
      <a class="link" :class="{doing: doing}" @click="download" href="itms-services://?action=download-manifest&url=https://cryptogalaxy.one/static/manifest.plist">Install iOS App</a>
      <a class="link" :class="{doing: doing}" @click="download" href="http://aq.pgyer.com/b0f3b49243a87f4a89083b38e8de3836.ipa?attname=CSR201811010613OHYCSG-resigned.ipa">Install iOS App</a>
    </div> -->
     <div class="Game-install-guide" @click="comeBack">
        {{$t("marketPlace.text28")}}
      </div>
    <div class="my-bd">
      <p class="prompt"> {{$t("banner.prompt1")}} </p>
      <a class="link" :class="{doing: doing}" @click="download" href="itms-services://?action=download-manifest&url=https://cryptogalaxy.one/static/ios/International/manifest.plist">{{$t("banner.prompt3")}}</a>
       <p class="prompt"> {{$t("banner.prompt2")}} </p>
      <a class="link" :class="{doing: doing}" @click="download" href="itms-services://?action=download-manifest&url=https://cryptogalaxy.one/static/ios/Asian/manifest.plist">{{$t("banner.prompt3")}}</a>
    </div>
    <div class="ft">
      <img class="footer-logo" src="@/assets/img/download_footer.png" alt="" />
    </div>
    </div>
    <GameInstallGuide  v-if="!isHlep" @comeBack="comeBack"/>
  </div>
</template>
<script>
import GameInstallGuide from './modules/gameInstallGuide';
export default {
  data() {
    return {
      doing: false,
      isHlep:true
    };
  },
  components:{
    GameInstallGuide
  },
    created(){
    //console.log(localStorage.getItem('lang'));
    if(localStorage.getItem('lang')){
       this.$i18n.locale = localStorage.getItem('lang');
    }
  },
  methods: {
    download() {
      this.doing = true;
    },
    comeBack(){
      this.isHlep =! this.isHlep;
    }
  }
};
</script>

<style lang="less" scoped>


@media only screen and (min-width: 751px) {
  @unit: 1px;
  @imgPath: "../../assets/img";

  .page {
    position: relative;
    width: 100%;
    background: url("@{imgPath}/download-bg.jpg") no-repeat center center ~"/" cover;
    .hd {
      padding-top: 160/@unit;
      .logo {
        width: 230 / @unit;
        height: 230 / @unit;
        display: block;
        margin: 0 auto 25 / @unit;
      }
      .title {
        font-weight: 500;
        font-size: 40 / @unit;
        color: #ffffff;
        line-height: 56 / @unit;
        text-align: center;
      }
      .version {
        font-weight: 300;
        font-size: 32 / @unit;
        color: #ffffff;
        line-height: 40 / @unit;
        margin-bottom: 42 / @unit;
        text-align: center;
      }
      .des {
        font-weight: 300;
        font-size: 26 / @unit;
        color: #ffffff;
        text-align: center;
      }
      .subdes {
        font-weight: 300;
        font-size: 18 / @unit;
        color: #ffffff;
        text-align: center;
      }
    }
    .Game-install-guide{
      text-align: center;
      font-size: 40 / @unit;
      color: #ffffff;
    }
    .my-bd{
      position:absolute;
      width:100%;
      padding:20px;
      box-sizing: border-box;
      bottom: 140/@unit;

      p{
         font-weight: 300;
        font-size: 18 / @unit;
        color: #ffffff;
        margin-bottom: 10 / @unit;
        text-align: center;
      } 
      a{
        margin-bottom: 40 / @unit;
        display: block;
        height: 90 / @unit;
        background: #70fec3;
        border-radius: 100 / @unit;
        font-weight: 500;
        font-size: 30 / @unit;
        color: #5068e3;
        text-align: center;
        line-height: 90 / @unit;
      }
    }
    .bd {
      .link {
        display: block;
        width: 660 / @unit;
        height: 90 / @unit;
        // position: absolute;
        // bottom: 250 / @unit;
        // left: 50%;
        // transform: translateX(-50%);
        margin-top: 90/@unit;
        position: relative;
        margin-left: auto;
        margin-right: auto;
        background: #70fec3;
        border-radius: 100 / @unit;
        font-weight: 500;
        font-size: 30 / @unit;
        color: #5068e3;
        text-align: center;
        line-height: 90 / @unit;
        &.doing {
          text-indent: -99999em;
          &::after {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            content: "";
            display: block;
            width: 36 / @unit;
            height: 36 / @unit;
            border: 4 / @unit solid rgba(0, 0, 0, 0);
            border-top-color: #fff;
            animation: circle 1s infinite linear;
            border-radius: 50%;
          }
        }
      }
    }

    .ft {
      padding-bottom: 60/@unit;
      .footer-logo {
        display: block;
        // position: absolute;
        width: 377 / @unit;
        margin: 60/@unit auto 0;
        // height: 144 / @unit;
        // bottom: 90 / @unit;
        // left: 50%;
        // transform: translateX(-50%);
      }
    }
  }
}


@media only screen and (max-width: 750px) {
  @unit: 70rem;
  @imgPath: "../../assets/img";

  .page {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url("@{imgPath}/download-bg.jpg") no-repeat center center ~"/" cover;

    .hd {
      .logo {
        width: 200 / @unit;
        height: 200 / @unit;
        display: block;
        margin: 100 / @unit auto 25 / @unit;
      }
      .title {
        font-weight: 500;
        font-size: 40 / @unit;
        color: #ffffff;
        line-height: 56 / @unit;
        text-align: center;
      }
      .version {
        font-weight: 300;
        font-size: 32 / @unit;
        color: #ffffff;
        line-height: 40 / @unit;
        margin-bottom: 42 / @unit;
        text-align: center;
      }
      .des {
        font-weight: 300;
        font-size: 26 / @unit;
        color: #ffffff;
        text-align: center;
      }
      .subdes {
        font-weight: 300;
        font-size: 18 / @unit;
        color: #ffffff;
        text-align: center;
      }
    }
     .Game-install-guide{
      text-align: center;
      font-size: 26 / @unit;
      color: #ffffff;
      text-decoration: underline;
      cursor: pointer;
       margin-top:60 / @unit; 
    }
  .my-bd{
      position:absolute;
      width:100%;
      padding:20px;
      box-sizing: border-box;
      bottom: 110/@unit;

      p{
         font-weight: 300;
        font-size: 18 / @unit;
        color: #ffffff;
        margin-bottom: 10 / @unit;
        text-align: center;
      } 
      a{
        margin-bottom: 30 / @unit;
        display: block;
        height: 80 / @unit;
        background: #70fec3;
        border-radius: 100 / @unit;
        font-weight: 500;
        font-size: 30 / @unit;
        color: #5068e3;
        text-align: center;
        line-height: 80 / @unit;
      }
    }
    .bd {
      .link {
        display: block;
        width: 660 / @unit;
        height: 80 / @unit;
        position: absolute;
        bottom: 250 / @unit;
        left: 50%;
        transform: translateX(-50%);
        background: #70fec3;
        border-radius: 100 / @unit;
        font-weight: 500;
        font-size: 30 / @unit;
        color: #5068e3;
        text-align: center;
        line-height: 80 / @unit;
        &.doing {
          text-indent: -99999em;
          &::after {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            content: "";
            display: block;
            width: 36 / @unit;
            height: 36 / @unit;
            border: 4 / @unit solid rgba(0, 0, 0, 0);
            border-top-color: #fff;
            animation: circle 1s infinite linear;
            border-radius: 50%;
          }
        }
      }
    }

    .ft {
      .footer-logo {
        display: block;
        position: absolute;
        width: 377 / @unit;
        // height: 144 / @unit;
        bottom: 60 / @unit;
        left: 50%;
        transform: translateX(-50%);
      }
    }
  }
}

@keyframes circle {
  0% {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
</style>

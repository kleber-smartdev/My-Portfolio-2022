<template>
 <div :class="`${heroBG} + `">
  <div class="hero-overlay animate__animated animate__bounceInDown animate__delay-1s">
    <div class="divider"></div>
    <nav>
        <el-row>        
          <el-col :span="8">
            <div class="logo">
                <img src="@/assets/logo.svg" />
            </div>
          </el-col>
          <el-col :span="16">
            <el-button type="primary" round><router-link to="/">Home</router-link></el-button>
            <el-button round><router-link to="/about">About</router-link></el-button>
            <el-button round><router-link to="/about">About</router-link></el-button>
            <el-button round><router-link to="/about">About</router-link></el-button>
            <el-button round><router-link to="/about">About</router-link></el-button>
            <el-button round><router-link to="/about">About</router-link></el-button>
          </el-col>
        </el-row>
      </nav>  
  </div>
</div>
</template>


<script lang="ts">
import { Vue } from 'vue-class-component';

export default class NavBar extends Vue {

// Random Background Banner
private index = 0;

private imagesBG = [
  "hero-bg-image-1",
  "hero-bg-image-2",
  "hero-bg-image-3",
  "hero-bg-image-4",
  "hero-bg-image-5",
  "hero-bg-image-6",
  "hero-bg-image-7"
];

private heroBG = this.imagesBG [this.index];

mounted() {
  this.index = Math.floor(Math.random() * this.imagesBG.length);
  this.heroBG = this.imagesBG[this.index];
  }
}
</script>


<style scoped>
/* NavBar CSS */
.divider {
  height: 30px;
}

.hero-overlay {
  height: 800px;
  background-color: rgba(0, 0, 0, 0.85);
}

.hero-overlay-1 {
  height: 800px;
  background-color: rgba(255, 255, 255, 0.85);
}

.hero-bg-image-1 {
  background-image: url('@/assets/background-images/saopaulo-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-2 {
  background-image: url('@/assets/background-images/vancouver-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-3 {
  background-image: url('@/assets/background-images/ottawa-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-4 {
  background-image: url('@/assets/background-images/saopaulo-2.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-5 {
  background-image: url('@/assets/background-images/vancouver-2.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-6 {
  background-image: url('@/assets/background-images/ottawa-2.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.hero-bg-image-7 {
  background-image: url('@/assets/background-images/saopaulo-3.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
    -webkit-animation: myBanner 0.33s ; /* Chrome, Safari, Opera */
    animation: myBanner 0.33s ;
  }

.logo {
  display: flex;
}

@media screen and (max-width: 550px) {
  .topnav.responsive {position: relative;}
  .topnav.responsive .icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
}

  /* Chrome, Safari, Opera */
  @-webkit-keyframes myBanner {
    from {filter: blur(50px);}
    to {filter: blur(0);}
  }

  /* Standard syntax */
  @keyframes myBanner {
    from {filter: blur(50px);}
    to {filter: blur(0);}
  }

</style>
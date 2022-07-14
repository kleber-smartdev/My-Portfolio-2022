<template>
 <navBar />
    <div class="container">   
        <div class="common-layout">        
            <el-container>
                  <el-header>
                      
                      <heroSection />
                  </el-header>
                  <el-main>
                      <router-view />
                      <mainSection />
                  </el-main>
            </el-container>
        </div>
    </div>
    <footerBar />

</template>


<script lang="ts">
import navBar from '@/components/NavBar.vue'
import heroSection from '@/components/HeroSection.vue'
import mainSection from '@/components/MainSection.vue'
import footerBar from '@/components/FooterBar.vue'

export default {
    components: { navBar, heroSection, mainSection, footerBar }
  }
</script>

<style>
/* Root CSS */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;600;800&display=swap');

* {
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    margin: 0 auto;
    padding: 0;
}

:root {
  --custom-light: #ccc;
  --custom-dark:  #2c3e50;
  --custom-white: #f1f1f1;
  --custom-link-dark: #222;
  --custom-link-light: #ccc;
  --custom-green: #414f41;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: var(--custom-dark); 
  color: var(--custom-white);
}

body {
  background-color: var(--custom-dark); 
  color: var(--custom-white);
}

.container {
  width: 99vw;
  padding: 5px;  
}

a {
  text-decoration: none;
  color: var(--custom-white);
  font-weight: bold;
}

a:hover {
  border-bottom: 3px solid var(--custom-white);
  border-radius: 4px;
  margin-top: 4px;
}

a:focus {
  border-bottom: 3px solid var(--custom-white);
  border-radius: 4px;
  margin-top: 4px;
}

a:visited {
  color: var(--custom-white);
  font-weight: bold;
}

/* .el-header {
  background: red;
}
.el-main {
  background-color: rgb(127, 89, 19);
}
.el-footer {
  background-color: rgb(106, 106, 13);
} */
</style>
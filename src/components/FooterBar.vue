<template>
    <footer>
        <div class="hr-footer-top"><!--Green divider --></div>
        <el-footer>
        <el-row>
            <el-col :xs="24" :sm="8" :md="12" :lg="18" :xl="18" class="el-col-align-left">
                <a href="https://kleberux.com" alt="Portfolio" title="Portfolio">
                    <h1>Kleber Sousa</h1>
                    UX / UI Designer & Frontend Developer
                </a>
            </el-col>
            <el-col :xs="24" :sm="4" :md="3" :lg="1" :xl="1" class="el-col-align-right">
                <a href="mailto:kleber.sousa@yahoo.com" target="_blank">                                        
                    <i class="icons fa fa-envelope" aria-hidden="true" alt="Email" title="Email"></i>
                </a>
            </el-col>
            <el-col :xs="24" :sm="4" :md="3" :lg="1" :xl="1" class="el-col-align-right">
                <a href="https://www.instagram.com/kleberux/" target="_blank">
                    <i class="icons fa fa-instagram" aria-hidden="true" alt="Instagram" title="Instagram"></i>
                </a>
            </el-col>
            <el-col :xs="24" :sm="4" :md="3" :lg="1" :xl="1" class="el-col-align-right">
                <a href="https://linkedin.com/in/klebersousa" target="_blank">
                    <i class="icons fa fa-linkedin" aria-hidden="true" alt="Linkedin" title="Linkedin"></i>
                </a>
            </el-col>
            <el-col :xs="24" :sm="4" :md="3" :lg="1" :xl="1" class="el-col-align-right">
                <a href="https://github.com/kleber-smartdev" target="_blank">
                    <i class="icons fa fa-github" aria-hidden="true" alt="GitHub" title="GitHub"></i>
                </a>
            </el-col>
            <el-col :xs="24" :sm="24" :md="24" :lg="24" :xl="24" class="el-col-align-center">
                Vancouver, Canada<br>&copy; {{ yearComplete }} Kleber UX.
            </el-col>
        </el-row>
        </el-footer>
    </footer>     
</template>


<script lang="ts">
export default {
  name: "getYear",
  setup() {
    return { yearComplete: new Date().getFullYear() };
  },
};
</script>


<style scoped>
/* FooterBar CSS */
.hr-footer-top {
    background-color: var(--custom-light);
    height: 35px;
    box-shadow: 0 1px 6px 0 rgb(32 33 36 / 28%);
}

footer {
    background-color: var(--custom-green);
    font-size: 0.75rem;
    position: relative;
    bottom: 0;
    height: auto;
    padding-bottom: 15px;
}

el-footer {
    background-color: var(--custom-green);
}

.el-col-align-left {
    align-items: left;
}

.el-col-align-right {
    align-items: right;
}

.el-col-align-center {
    align-items: center;
}

.icons {
    font-size:1.6rem;
    color: var(--custom-white);
}

i:hover {
    color: gold;
}

@media screen and (max-width: 778px) {
    .el-col-align-center {
        align-self: left;
    }
    .el-col-align-right {
        align-self: left;
    }
}
</style>
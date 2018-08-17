<template>
    <nav class="navbar menu-bg is-fixed-top" role="navigation" aria-label="main navigation">
        <a class="navbar-item p-left-20" @click="toggleNav()">
            <i class="fa fa-bars fa-2x"></i>
        </a>
        <a class="navbar-item">
            <img src="https://bulma.io/images/made-with-bulma.png">
        </a>
        <div class="navbar-item header-title">
            <h2 style="color:#37617A;">My Admin Panel</h2>
        </div>
        <div class="navbar-end">
            <div class="navbar-item" >
                <i class="fa fa-bell fa-2x"></i>
            </div>
            <div class="navbar-item">                
                    User Name                
            </div>
            <div class="navbar-item" >
                <i class="fa fa-power-off fa-2x"></i>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
  name: "top-nav-bar",
  data() {
    return {};
  },
  methods: {
    toggleNav() {
        this.$parent.$emit('toggleNav');
    }
  }
};
</script>
<style lang="scss" scoped>
.p-left-20{
    padding-left: 20px;
}
.header-title{
font-size:1.55em;
}
</style>



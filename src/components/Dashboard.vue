<template>
    <div class="columns is-fullheight">
        <div class="column is-2 is-sidebar-menu is-hidden-mobile is-margin-top-30" :class="getClass()" >
            <sidebar></sidebar>
        </div>
        <div class="column is-main-content is-left-gapless" style="background-color:#FFF;">
           <topnav></topnav>
           
           <div class="is-padding-20 is-margin-top-50" >  
            <p>Why do we use it? It is a long </p>
            <div class="container" style="background-color:#FF0000;">
                <AccordionMenu :contents="contents"></AccordionMenu>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
import Sidebar from "./layout/Sidebar.vue";
import Topnav from "./layout/Topnav.vue";

export default {
  name: "Dashboard",
  data() {
    return {
      active: true,
      
    };
  },
  components: {
    Sidebar,
    Topnav
  },
  mounted() {
    this.$on("toggleNav", () => {
      console.log("toggle received in Dashboard");
      this.active = !this.active;
    });
  },
  methods: {
    getClass() {
      if (this.active === true) {
        return "is-active-sidebar";
      } else {
        return "is-hide-sidebar";
      }
    }
  }
};
</script>


<style lang="scss" scoped>
$grey-darker: hsl(0, 0%, 21%) !default;
$grey-dark: hsl(0, 0%, 29%) !default;
$grey: hsl(0, 0%, 48%) !default;
$grey-light: hsl(0, 0%, 71%) !default;
$grey-lighter: hsl(0, 0%, 86%) !default;
$navbar-height: 3rem;

.is-sidebar-menu {
  padding: 2.5rem;
  background: #f8f7f5;
}
.menu-bg {
  background: #f8f7f5;
}
.columns,
is-fullheight {
  min-height: calc(100vh - (#{$navbar-height} - 0.65rem));
  max-height: calc(100vh - (#{$navbar-height} - 0.65rem));
  height: calc(100vh - (#{$navbar-height} - 0.65rem));
  display: flex;
  flex-direction: row;
  justify-content: stretch;
  .column {
    overflow-y: auto;
  }
}
.is-main-content {
  background: #ffffff;
}
.is-left-gapless {
  padding-left: 0rem;
}

.is-show-sidebar {
  display: block;
  //  visibility: visible;
  //   opacity: 1;
  //   transition-delay: 0s;
}
.is-hide-sidebar {
  display: none;
  // visibility: collapse;
  // opacity: 0;
  // transition: visibility 3s linear 0.75s, opacity 0.75s linear;
}
.is-margin-top-30 {
  margin-top: 30px;
}
.is-margin-top-50 {
  margin-top: 50px;
}
.is-padding-20 {
  padding: 20px;
}
.dashboard-container {
  overflow-y: scroll;
}
.hero-padding{
  padding: 1rem 1rem;
}
</style>



<template >
    <aside class="menu">
        <p class="menu-lable-text is-size-6">
            General
        </p>
        <ul class="menu-list">
            <li><a>Dashboard</a></li>                   
        </ul>
        <p class="menu-lable-text is-size-6">
            Administration
        </p>
        <ul class="menu-list">
            <li><a>Admin Task 1</a></li>            
             <li><a>Admin Task 2</a></li>
            <li><a>Admin Task 3</a></li>
            <li><a>Admin Task 4</a></li>
            <li><a>Admin Task 5</a></li>
            <li><a>Admin Task 6</a></li>
            <li><a>Admin Task 7</a></li>
        </ul>
        <p class="menu-lable-text is-size-6">
            Communication
        </p>
        <ul class="menu-list">
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
            <li><a>Communication1</a></li>
        </ul>
   </aside>
</template>

<script>
export default {
  name: "side-bar",
  data() {
    return {
      active: true
    };
  },
  prop: {},
  mounted() {},
  methods: {}
};
</script>



<style lang="scss">
.menu-lable-text {
  color: #40c1bb;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}
.menu-lable-text:not(:last-child) {
  margin-bottom: 0.85em;
}
</style>
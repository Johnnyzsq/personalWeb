<template>
  <link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css"
  />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
  />
  <div class="part1" v-if="!show">
    <button class="btn btn-outline-success" type="button" @click="open">
      <i class="bi bi-ui-radios" style="font-size: 3rem; color: #ffffff;" ></i>
    </button>
  </div>
  <transition
    enter-active-class="animate__animated animate__zoomIn"
    leave-active-class="animate__animated animate__zoomOut"
  >
    <nav v-if="show">
      <ul class="sub-menu">
        <li class="d-flex flex-row-reverse btn-lg">
          <button type="button" class="btn-close" aria-label="Close" @click="close"></button>
        </li>
        <li class="d-flex flex-row-reverse" @click="close">
            <router-link to="/">Home <i class="bi bi-house-door-fill"></i> </router-link>
        </li>
        <li class="d-flex flex-row-reverse" @click="close">
          <router-link to="/about">About Us <i class="bi bi-person-lines-fill"></i></router-link>
        </li>
        <li class="d-flex flex-row-reverse" @click="close">
          <router-link to="/work">My Work <i class="bi bi-server"></i></router-link>
        </li>
        <li class="d-flex flex-row-reverse" @click="close">
          <router-link to="/contact">Contact Us <i class="bi bi-card-heading"></i></router-link>
        </li>
        
      </ul>
    </nav>
  </transition>

  <router-view />
</template>
<script>
// @ is an alias to /src

export default {
  data(){
    return{
      show:false
    }
  },
  methods:{
    open(){
      this.show =! this.show
    },
    close(){
      this.show =! this.show
    }
  }
}
</script>

<style lang="scss" scope>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
}
.part1 {
  display: flex;
  z-index: 1;
  position: absolute;
  top: 0px;
  right: 0px;
  .btn {
    margin: 40px 20px;
  }
}
nav {
  display: flex;
  z-index: 1;
  position: absolute;
  top: 0px;
  right: 0px;
  width: 350px;
  height: 350px;
  border-radius: 50% 0px 50% 50% ;
  background-color: #4EBD87;
  color: rgb(255, 255, 255);
  a {
    font-weight: bold;
    color: #ffffff;
    font-size: 24px;
    text-decoration: none;
    &.router-link-exact-active {
      color: #fcca00;
    }
  }
  .sub-menu {
    width: 300px;
    height: 300px;
    margin-top: 30px;
    list-style: none;
    li {
      padding: 8px;
      font-weight: 400;
    }
  }
}
</style>

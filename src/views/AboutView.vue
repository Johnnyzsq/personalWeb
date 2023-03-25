<template>
  <div class="contact">
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
    />
    <transition class="animate__animated animate__slideInRight">
      <div class="main">
        <div class="jianli" v-if="show">
          <div class="part1"></div>
          <div class="part2"></div>
        </div>
        <div class="key " v-if="!show">
          <h1>查看简历</h1>
          <div class="form-floating d-flex">
            <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea" v-model="key"></textarea>
            <label for="floatingTextarea">Place input your key</label>
         <button type="button" class="btn btn-warning btn-lg"  @click="enter">OK</button>

          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  data() {
    return {
      show: false,
      key:""
    };
  },
  methods: {
    enter(){
      if(this.key == "123456" ){
       this.show =true
      }else{
        alert("密钥错误！")
      }
    }
  }
};
</script>
<style scoped lang="scss">
.contact {
  .main {
    width: 100%;
    height: 760px;
    background: url(@/assets/1003.jpg);
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    .key{
      .form-floating{
        .form-control{
          width: 450px;
        }
      }
      button{
        width: 100px;
      }
      h1{
        color: #ffffff;
      }
    }
    .jianli {
      width: 90%;
      height: 700px;
      .part1 {
        width: 500px;
        height: 700px;
        background-color: aqua;
        margin: 30px 260px 0px 0px;
        border-radius: 20px;
        background: url(@/assets/Screenshot_10.png) no-repeat;
        background-size: 100% 100%;
      }
      .part2 {
        width: 500px;
        height: 700px;
        background-color: aqua;
        margin: 0px 0px 0px 180px;
        border-radius: 20px;
        background: url(@/assets/Screenshot_9.png) no-repeat;
        background-size: 100% 100%;
      }
    }
  }
}
</style>  
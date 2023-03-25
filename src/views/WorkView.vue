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
    <transition class="animate__animated animate__slideInLeft">
      <div class="main">
        <div class="card" style="width: 38rem;">
          <img src="@/assets/1005.jpg" class="card-img-top" alt="..." />
          <div class="card-body">
            <h5 class="card-title">我的个人项目与作品</h5>
            <p
              class="card-text"
            >主要完成了前端方面的开发。应用的前端技术主要有vue3.0全家桶、uniapp 开发技术、bootstrapIU、uviewUI 、vantUI开发组件库。
            后台数据主要采用的是通过 Request和Axious 获取 Apifox 和Postman云端数据。</p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">个人作品"Carpo—汽车商城"：<a href="https://gitee.com/zhu-shengqiang/carpo-auto-mall">https://gitee.com/zhu-shengqiang/carpo-auto-mall</a></li>
            <li class="list-group-item">个人作品“农乡桃花源”：<a href="https://gitee.com/zhu-shengqiang/rural-taohuayuan">https://gitee.com/zhu-shengqiang/rural-taohuayuan</a></li>
            <li class="list-group-item">个人作品“LY旅游APP“：<a href="https://gitee.com/zhu-shengqiang/ly-travel-app">https://gitee.com/zhu-shengqiang/ly-travel-app</a></li>
          </ul>
          <div class="card-body">
            <a href="#" class="card-link">Thank you</a>
            <a href="#" class="card-link">Hope like</a>
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
    return {};
  },
  methods: {}
};
</script>
<style scoped lang="scss">
.contact {
  .main {
    width: 100%;
    height: 760px;
    background: url(@/assets/1004.jpg);
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>  
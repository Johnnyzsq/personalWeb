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
    <transition class="animate__animated animate__slideInDown">
      <div class="main">
        <div class="list-group">
          <a
            href="#"
            class="list-group-item list-group-item-action active"
            aria-current="true"
          >我的联系方式</a>
          <a href="#" class="list-group-item list-group-item-action">我的微信:ZSQUFC</a>
          <a href="#" class="list-group-item list-group-item-action">我的邮箱:1926937936@qq.com</a>
          <a href="#" class="list-group-item list-group-item-action">我的QQ:1926937936</a>
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
    background: url(@/assets/1006.jpg);
    display: flex;
    justify-content: center;
    align-items: center;
    .list-group{
      width: 40%;
    }
  }
}
</style>
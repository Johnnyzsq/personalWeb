<template>
  <div class="home">
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
    />
    <transition class="animate__animated animate__slideInUp">
      <div class="main">
        <div
          id="carouselExampleIndicatorsy"
          class="carousel slide carousel-fade"
          data-bs-ride="carousel"
          data-bs-pause="false"
          data-bs-interval="2000"
        >
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img src="@/assets/1005.jpg" class="d-block w-100" alt="..." />
            </div>
            <div class="carousel-item">
              <img src="@/assets/1002.jpg" class="d-block w-100" alt="..." />
            </div>
            <div class="carousel-item">
              <img src="@/assets/1001.jpg" class="d-block w-100" alt="..." />
            </div>
          </div>
        </div>

        <div class="content">
          <div class="tip">
            <i class="bi bi-x-diamond-fill" style="font-size: 2rem; color: #ffffff;">----欢迎您的到来</i>
          </div>
          <div class="part1">
            <p>
              <button
                class="btn btn-outline-warning btn-lg"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#collapseWidthExample"
                aria-expanded="false"
                aria-controls="collapseWidthExample"
              >我是谁？</button>
            </p>
            <div style="min-height: 120px;">
              <div class="collapse collapse-horizontal" id="collapseWidthExample">
                <div
                  class="card card-body"
                  style="width: 300px;"
                >我是一名乐于积累经验，热爱互联网行业。有快速学习能力、上进心强和良好的团队合作精神的有志青年。</div>
              </div>
            </div>
          </div>
          <div class="part2">
            <h1>朱圣强(Johnny)</h1>
            <div class="text-scroll">
              <ul class="marquee-list" :class="{'animate-up': animateUp}">
                <li v-for="(item, index) in listData" :key="index">{{item}}</li>
              </ul>
            </div>
            <h5>
              我很喜欢一句话“生命在于探索与创造，虽然有时需要用八分的奋发来赢取两分的机会，但请永远保持年轻和好奇”。
            </h5>
            <div class="mylove">
              <div class="get">
                <i class="bi bi-life-preserver" style="font-size: 3rem; color: #ffffff;"></i>
                <h5>LOVE LIFE</h5>
              </div>
              <div class="get">
                <i class="bi bi-bar-chart-line-fill" style="font-size: 3rem; color: #ffffff;"></i>
                <h5>WILLING LEARN</h5>
              </div>
              <div class="get">
                <i class="bi bi-hand-index-thumb-fill" style="font-size: 3rem; color: #ffffff;"></i>
                <h5>RESPONS</h5>
              </div>
              <div class="get">
                <i class="bi bi-emoji-smile-fill" style="font-size: 3rem; color: #ffffff;"></i>
                <h5>EXPLORATION</h5>
              </div>
            </div>
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
      animateUp: false,
      listData: [
        "快速学习能力，责任感强烈",
        "能承受压力和及时完成任务",
        "做事耐心细致，乐于探索"
      ],
      timer: null
    };
  },
  mounted() {
    this.timer = setInterval(this.scrollAnimate, 1500);
  },
  methods: {
    shot() {
      this.show = !this.show;
    },
    scrollAnimate() {
      this.animateUp = true;
      setTimeout(() => {
        this.listData.push(this.listData[0]);
        this.listData.shift();
        this.animateUp = false;
      }, 500);
    }
  }
};
</script>
<style scoped lang="scss">
.main {
  width: 100%;
  img {
    width: 100%;
    height: 760px;
  }
}
.content {
  position: absolute;
  display: flex;
  z-index: 1;
  top: 30px;
  left: 100px;
  width: 70%;
  height: 700px;
  text-align: start;
  .tip {
    width: 400px;
    height: 100px;
    display: flex;
  }
  .part1 {
    margin-top: 100px;
    width: 100%;
    height: 100px;
  }
  .part2 {
    margin-top: 200px;
    width: 100%;
    height: 450px;
    color: #ffffff;
    h1 {
      font-size: 68px;
      font-weight: 600;
    }
    .text-scroll {
      height: 30px;
      ul {
        height: 26px;
        overflow: hidden;
      }
    }
    .mylove {
      height: 250px;
      display: flex;
      justify-content: space-around;
      .get {
        width: 150px;
        height: 150px;
        border: #ffffff 2px solid;
        margin-top: 40px;
        text-align: center;
        line-height: 80px;
      }
      .get:hover {
        transform: rotate(-45deg);
      }
    }
  }
}
</style>
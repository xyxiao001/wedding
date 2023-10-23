<script>
  import { onMount } from 'svelte'

  let videoEle
  let player

  onMount(async () => {
    const width = videoEle.offsetWidth;

    player = new Player({
      id: 'vlog',
      url: 'https://p6-addone-sign.byteimg.com/tos-cn-i-hhc0kcolqq/ddd87d8147e044388535c2e0e7bf6844.jpg~tplv-hhc0kcolqq-image.image?x-expires=2013407255&x-signature=ajy3QREDxgCpFccN4%2Fo%2FHL9htLA%3D',
      poster: 'https://p6-addone-sign.byteimg.com/tos-cn-i-hhc0kcolqq/27d22382a1c746e0b3cd49cd16831644.jpg~tplv-hhc0kcolqq-image.image?x-expires=2013407099&x-signature=vHy4EV9hVV50Jp0G1k1RurO%2BDpI%3D',
      controlPlugins: [],
      fitVideoSize: 'auto',
      width: width,
      height: (width * 9) / 16,
      playsinline: true,
    })
  })
</script>

<main class="container intro pt-52px pl-33px pb-25px">
  <header class="relative">
    <div class="flex items-center">
      <img src="/assets/xi.svg" class="text-red-500" alt="囍" />
      <p class="whats-it ml-2px">Wedding invitation of B&O</p>
    </div>

    <div class="absolute -right-30px top-0">
      <div class="magic-circle opacity-89 rounded-1/2  right-0" />
      <div class="magic-circle opacity-67 right-23px rounded-1/2" />
      <div class="magic-circle opacity-20 right-40px rounded-1/2" />
    </div>

    <div class="mt-35px">
      <h1 class="our-name">廖创</h1>
      <div class="h-28px">
        <img
          src="./assets/BruceandOrage.svg"
          class="b-n-o"
          alt="Bruce and Orange"
        />
      </div>

      <h1 class="our-name">唐银涛</h1>
    </div>

    <div class="separator w-156px h-1px" />
  </header>

  <section class="pt-25px content relative">
    <img
      class="absolute right-25px top-20px fern"
      width="40px"
      src="https://wedding-1307329121.file.myqcloud.com/fern.png?imageMogr2/thumbnail/!50p"
      alt=""
    />
    <div class="sentence">
      <h4>诚邀您来参加我们的婚礼派对！</h4>
      <p>Invite you to join our marrige party.</p>
    </div>
    <h5 class="which-day mt-10px mb-12px">2024.02.13 正月初四</h5>
    <div class="sentence">
      <h4 class="location relative">
        湖北省天门市岳口镇
      </h4>
      <p>Yuekou Town, Tianmen City, Hubei Province</p>
    </div>
  </section>
</main>

<main bind:this={videoEle} class="container vlog" id="vlog" />

<main class="container process pt-47px px-21px">
  <h2 class="process-title">婚礼流程</h2>
  <p>Schedule of the day.</p>

  <ul class="steps">
    <li class="step-item">
      <h4 class="step-title">10:30 · 草坪签到</h4>
      <div class="step-details">
        到达酒店后根据指引牌在草坪签到，并领取游园会敲章卡
      </div>
    </li>
    <li class="step-item">
      <h4 class="step-title">11:00 · 游园会×仪式</h4>
      <div class="step-details">
        我们为大家准备了些小游戏和饮品，也会通过简单快乐的
        方式，让大家相信这俩人结婚后一定会幸福啊～
      </div>
    </li>
    <li class="step-item">
      <h4 class="step-title">12:00 · 准备进酒店开始午宴</h4>
      <div class="step-details">
        我们的午餐安排的有点晚，大家记得在游园会上先吃点哦
      </div>
    </li>
  </ul>

  <div class="hint">
    <div>着装建议：如果您能穿浅色系的衣服来，就更棒啦</div>
  </div>

  <div class="douyin-live">
    <img
      class="w-full relative z-10"
      src="https://wedding-1307329121.file.myqcloud.com/qr-group.jpg"
      alt=""
    />
  </div>

  <div class="douyin-text">
    抖音扫码可观看婚礼直播<br />直播间 ID: 921201364
  </div>
</main>

<footer class="container gallery relative">
  <div class="mask" />
  <img src="/assets/BruceandOrange.svg" class="ending" alt="Bruce and Orange" />
  <img src="https://p6-addone-sign.byteimg.com/tos-cn-i-hhc0kcolqq/ddd87d8147e044388535c2e0e7bf6844.jpg~tplv-hhc0kcolqq-image.image?x-expires=2013407255&x-signature=ajy3QREDxgCpFccN4%2Fo%2FHL9htLA%3D" width="100%" alt="" />
</footer>

<style>
  .container {
    width: 100%;
    margin: 0 auto;
    overflow: hidden;
    background-color: var(--primary-color);
  }
  @media (min-width: 558px) {
    .container {
      max-width: 500px !important;
    }
  }
  .intro {
    background-color: #fff;
  }
  p {
    font-family: 'Source Serif Pro', serif;
  }
  h1,
  h2,
  h4,
  h5 {
    font-family: '思源宋体 CN', serif;
  }
  .whats-it {
    display: block;
    font-size: 8.5px;
    line-height: 18px;
    transform: translateY(1px);
    text-decoration: underline;
  }
  .b-n-o {
    margin-top: 6px;
    margin-bottom: -4px;
    color: var(--primary-color);
  }
  .our-name {
    font-size: 40px;
    line-height: 57px;
    font-weight: 600;
  }
  .magic-circle {
    position: absolute;
    top: 0;
    width: 98px;
    height: 98px;
    background-color: var(--primary-color);
  }
  .separator {
    margin-top: 58px;
    background-color: #111;
    transform: scaleY(0.7);
  }
  .which-day {
    font-size: 32px;
    line-height: 44px;
  }
  .sentence > h4 {
    font-size: 14px;
    line-height: 20px;
  }
  .sentence > p {
    font-size: 12px;
    line-height: 14px;
  }
  .location::before {
    position: absolute;
    left: -14px;
    top: 2px;
    content: url(/assets/location.svg);
  }
  #vlog {
    overflow: hidden;
  }
  #vlog::after {
    content: '';
    display: block;
    padding-bottom: 56.25%;
    background-color: #111;
  }
  .process {
    color: white;
    padding-bottom: 75px;
  }
  .process > h2 {
    font-size: 25px;
    line-height: 36px;
    font-weight: 600;
  }
  .process > p {
    font-size: 10px;
    line-height: 14px;
    text-decoration: underline;
  }
  .steps {
    margin-top: 43px;
    padding-left: 11px;
  }
  .step-item {
    margin-bottom: 33px;
  }
  .step-title {
    position: relative;
    font-size: 16px;
    line-height: 21px;
    font-weight: 600;
  }
  .step-title::before {
    position: absolute;
    left: -16px;
    top: 4px;
    content: '';
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: var(--secondary-color);
  }
  .step-details {
    margin-top: 5px;
    font-size: 13px;
    line-height: 17px;
    font-weight: 300;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .hint {
    font-size: 13px;
    line-height: 17px;
    padding-left: 12px;
    color: var(--secondary-color);
  }
  .douyin-live {
    position: relative;
    width: 44%;
    height: 44%;
    margin: 83px auto 40px;
  }
  .douyin-text {
    font-size: 11px;
    line-height: 14px;
    font-weight: 300;
    text-align: center;
  }
  .gallery {
    background-color: var(--primary-color);
  }
  .mask {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
    /* background-color: var(--primary-color); */
    background-image: linear-gradient(
      180deg,
      var(--primary-color) 0%,
      rgba(97, 106, 88, 0.4) 100%,
      transparent 150%
    );
    background-size: 100% 100%;
    /* opacity: 0.7; */
  }
  .ending {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 30px;
    width: 35%;
    margin: 0 auto;
  }
</style>

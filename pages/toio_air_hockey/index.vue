<template>
  <div class="toio-air-hockey">
    <header class="theBridge">
      <img src="./assets/title.jpg" alt="対戦！toio エアホッケー" />
    </header>
    <main>
      <div class="top-section-wrapper milkyWay">
        <div class="main-image" style="clip-path: polygon(100% 0%, 100% 80%, 50% 100%, 0 80%, 0 0)">
          <img src="./assets/main-image.jpg" alt="対戦！toio エアホッケー" />
        </div>

        <section class="section">
          <div class="overview">
            <div class="left">
              <h2>
                「対戦！toio エアホッケー」とは、<br /><a
                  href="https://protopedia.net/event/13?link=externallink"
                  target="_blank"
                  >toio の「Do!コン」</a
                >というプログラミングコンテストにて、<br />銀賞を受賞した作品になります。
              </h2>
              <div class="mt-16" style="text-align: left">
                <p>
                  toio Do
                  「Do!コン」とは、『子どもたちの「おうち時間」が笑顔でいっぱいになる』というテーマのプログラミングコンテストです。
                </p>
                <p>toio を使って toio Do 上でエアーホッケーをプレイできます。</p>
              </div>
              <div class="mt-8" style="text-align: left">
                <p>
                  作品サイト(toio Do)：<a href="https://toio.io/do/play/td1p0081" target="_blank"
                    >https://toio.io/do/play/td1p0081</a
                  >
                </p>
              </div>
            </div>
            <div class="right">
              <img src="./assets/img3.jpg" alt="" />
            </div>
          </div>
        </section>
      </div>

      <section class="section milkyWay">
        <iframe
          src="https://www.youtube.com/embed/FW9hcF-PZfA"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </section>

      <section class="section milkyWay">
        <div class="overview">
          <div class="left">
            <h2>用意するもの</h2>
            <div class="mt-16" style="text-align: left">
              <p>toio 基本セットのみ！</p>
              <p>詳しくは、<a href="https://toio.io/do/play/td1p0081" target="_blank">作品サイト</a>をご確認ください。</p>
            </div>
          </div>
          <div class="right">
            <img src="./assets/img2.jpg" alt="" />
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component({
  name: 'ToioAirHockey',
  layout: 'chibi929-app',
  head: {
    title: 'ToioAirHockey',
  },
  components: {},
})
export default class ToioAirHockey extends Vue {}
</script>

<style lang="scss" scoped>
iframe {
  width: 720px;
  height: calc(720px * 9 / 16);
  @include sp() {
    width: 100%;
    height: calc(var(--window-width) * 9 / 16);
  }
}
.toio-air-hockey {
  text-align: center;

  main {
    height: calc(100% - 6rem);

    section {
      padding: 2rem;
    }

    .section {
      ul {
        margin-left: 2.5rem;
      }
    }
  }

  .main-image {
    height: 48rem;
    background-color: $color_black;
    img {
      max-width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  .overview {
    @include sp() {
      min-width: 100%;
      flex-direction: column-reverse;
    }
    display: flex;
    width: 75%;
    min-width: 86rem;
    margin: 0 auto;
    padding: 1rem;
    background-color: $color_white;
    border-radius: 1rem;

    .left {
      @include sp() {
        width: 100%;
      }
      width: 50%;
      padding: 2rem;
      text-align: left;
    }

    .right {
      @include sp() {
        width: 100%;
      }
      width: 50%;
      padding: 2rem;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    img {
      width: 38.4rem;
    }
  }

  .for-example {
    @include sp() {
      flex-wrap: wrap;
    }
    display: flex;
    justify-content: center;
    margin-top: 1.2rem;

    div.content {
      &:not(:first-child) {
        margin-left: 2rem;
      }
      @include sp() {
        &:not(:first-child) {
          margin-left: 0rem;
          margin-top: 2rem;
        }
        width: 100%;
        min-width: 100%;
        max-width: 100%;
      }

      text-align: left;
      width: 25%;
      min-width: 25%;
      max-width: 25%;
      padding: 2rem;

      background-color: $color_white;
      border-radius: 1rem;

      .image-wrapper {
        text-align: center;
        img {
          width: 7.5rem;
        }
      }
    }
  }
}
</style>

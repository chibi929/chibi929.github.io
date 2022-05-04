<template>
  <div class="typing-quest">
    <header class="theBridge">
      <img src="./assets/title.png" alt="TypingQuest" />
    </header>
    <main>
      <div class="main-image">
        <img src="./assets/main-image.jpg" alt="TypingQuest" />
      </div>
      <section class="section milkyWay">
        <div class="overview">
          <div class="left">
            <h2>「タイピングクエスト」とは、<br />自分たちで描いた敵キャラクターを倒していくタイピングゲームです。</h2>
            <div style="text-align: left">
              <p>楽しくタイピングしたくありませんか？</p>
              <p>自分で描いたキャラクターがタイピングのお題になるのが特徴です。</p>
              <p>タイピング練習をするなら楽しくタイピングができれば良いなと思い制作しました。</p>
            </div>
          </div>
          <div class="right">
            <img src="./assets/neko.jpg" alt="" />
          </div>
        </div>
      </section>
      <section class="section milkyWay">
        <h2>例えばこんな感じ！</h2>
        <div class="for-example">
          <div class="content">
            <div class="image-wrapper">
              <img src="@/assets/images/point1.png" alt="ポイント1" />
            </div>
            <h3>楽しくタイピング練習したい！</h3>
            <ul>
              <li>クエスト風に敵を倒しながらタイピングを学べます。</li>
            </ul>
          </div>
          <div class="content">
            <div class="image-wrapper">
              <img src="@/assets/images/point2.png" alt="ポイント2" />
            </div>
            <h3>自分のキャラクターをタイピングゲームに登場させたい！</h3>
            <ul>
              <li>自分で描いたキャラクターが敵として登場します。</li>
              <li>キャラクターの名前をタイピングするゲームになります。</li>
            </ul>
          </div>
          <div class="content">
            <div class="image-wrapper">
              <img src="@/assets/images/point3.png" alt="ポイント3" />
            </div>
            <h3>友達と一緒にタイピングゲームを楽しみたい！</h3>
            <ul>
              <li>友達のキャラクターをタイピングで倒そう。</li>
              <li>自分のキャラクターを友達にタイピングしてもらおう。</li>
            </ul>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component({
  name: 'TypingQuest',
  layout: 'chibi929-app',
  head: {
    title: 'TypingQuest',
  },
})
export default class TypingQuest extends Vue {}
</script>

<style lang="scss" scoped>
.typing-quest {
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

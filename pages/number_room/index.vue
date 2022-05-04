<template>
  <div class="number-room">
    <header>
      <a href="https://mashandroom.org/"><img src="./mashandroom.png" alt="" /></a>
    </header>
    <main>
      <div class="main-image">
        <img src="./header.jpg" alt="" />
      </div>
      <section class="product">
        <div class="contents-wrapper" style="text-align: center">
          <a class="button" href="https://www.amazon.co.jp/chibi929/dp/B07GR6CSYV" target="_blank">Alexa 版へのリンク</a>
        </div>
      </section>
      <section class="about ice">
        <div class="contents-wrapper">
          <h1>「数字のお部屋」とは？</h1>
          <p>
            chibi929(kinoko929) が提供する Alexa スキルです。<br />
            このスキルは、1から100までの数字を数えられるように支援する子ども向けスキルになっています。<br />
            数字が少しずつ数えられるようになってきたお子さんへ。遊びながら100まで数えられるようになろう！
          </p>
        </div>
      </section>
      <section class="how-to">
        <div class="contents-wrapper">
          <h1>遊び方</h1>
          <h2>起動方法</h2>
          <p>「アレクサ、数字のお部屋を開いて」</p>
          <h2>遊び方</h2>
          <p>
            起動をすると説明が始まります。<br />
            スキルの説明通り「1」から数えあげてください。<br />
            数字がちゃんと数えられると正解音とともに「次の数字は？」と促されますので「2」->「3」->「4」と次々と数えて下さい。<br />
            正しく数えられなかった場合は、不正解音と共に現在数え上げた数字を教えてくれますので、次の数字を言ってみてください。
          </p>
          <h2>ヒントモード</h2>
          <p>
            例えば「5」の次の数字がどうしてもわからない場合は「ヒント」と話しかけてみてください。<br />
            こっそり答えを教えてくれます。<br />
            例: 《今「5」まで数えたから、次は「6」だよ！言ってみて》と教えてくれます。
          </p>
        </div>
      </section>
      <section class="privacy ice">
        <div class="contents-wrapper">
          <h1>プライバシーポリシー</h1>
          <p>
            chibi929(kinoko929) が提供する Alexa スキル「数字のお部屋」は、<br />
            スキルを有効化した際に生成されるランダム値(ユーザID)を利用してプレイ記録を保持しています。<br />
            <br />
            ご利用になる皆様の個人情報(お名前や生年月日など)やプライバシーに関わる情報は収集いたしません。
          </p>
          <p>2018年8月22日制定</p>
          <p>
            chibi929(kinoko929)<br />
            お問い合わせ先: <a href="mailto:kinoko929@mashandroom.org" target="_blank">kinoko929@mashandroom.org</a>
          </p>
        </div>
      </section>
    </main>
    <footer class="underTheEarth">
      <p>Copyright © 2018 chibi929 All Rights Reserved.</p>
    </footer>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component({
  name: 'NumberRoom',
  head: {
    title: '数字のお部屋',
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/number_room.ico' }],
  },
})
export default class NumberRoom extends Vue {
  private created(): void {
    console.log('created')
  }

  private mounted(): void {
    console.log('mounted')
  }
}
</script>

<style lang="scss" scoped>
.number-room {
  h1 {
    font-size: 2rem;
  }
  h2 {
    font-size: 1.5rem;
  }
  section {
    padding: 1rem;
  }

  div.main-image {
    max-height: 420px;
    img {
      max-height: 420px;
      width: 100%;
      object-fit: cover;
    }
  }

  a.button {
    display: inline-block;
    padding: 0.5em 1em;
    text-decoration: none;
    color: #fff;
    background-image: -webkit-linear-gradient(#6795fd 0%, #67ceff 100%);
    background-image: linear-gradient(#6795fd 0%, #67ceff 100%);
    border-radius: 20px;
  }
  a.button:active {
    background-image: -webkit-linear-gradient(#6795fd 0%, #67ceff 70%);
    background-image: linear-gradient(#6795fd 0%, #67ceff 70%);
  }

  header {
    height: 60px;
    img {
      height: 60px;
    }
  }
  footer {
    padding: 1rem;
    text-align: center;
  }
}
</style>

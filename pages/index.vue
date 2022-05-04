<template>
  <div class="index-page">
    <div class="profile">
      <img src="@/assets/images/chibi929.png" />
      <p>chibi929</p>
    </div>

    <div class="links">
      <a href="https://twitter.com/ibihc929">
        <img src="@/assets/images/twitter_logo.png" alt="Twitter" />
      </a>
      <a href="https://www.facebook.com/chibi929">
        <img src="@/assets/images/facebook_logo.png" alt="Facebook" />
      </a>
      <a href="https://github.com/chibi929">
        <img src="@/assets/images/github_logo.png" alt="GitHub" />
      </a>
      <a href="https://qiita.com/chibi929">
        <img src="@/assets/images/qiita_logo.png" alt="Qiita" />
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component({
  name: 'IndexPage',
})
export default class IndexPage extends Vue {
  private created(): void {
    console.log('created')
  }

  private mounted(): void {
    console.log('mounted')
  }
}
</script>

<style lang="scss">
html,
body,
#__nuxt,
#__layout {
  width: 100%;
  height: 100%;
}
</style>

<style lang="scss" scoped>
.index-page {
  height: 100%;
  background-color: #eeffee;
  text-align: center;

  .profile img {
    width: 128px;
  }

  .links {
    margin-top: 1rem;

    img {
      width: 32px;
    }
  }
}
</style>

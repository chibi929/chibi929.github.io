<template>
  <div class="chibi929-app-layout" :style="styles">
    <Nuxt class="page" />
    <footer class="theBridge">
      <small>Copyright © 2022- chibi929 All Rights Reserved.</small>
    </footer>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component
export default class Chibi929AppLayout extends Vue {
  private state: any = {
    pageSize: { width: 0, height: 0 },
  }

  private created(): void {
    window.addEventListener('resize', this.updatePageSize)
  }

  private mounted(): void {
    this.updatePageSize()
  }

  private beforeUnmount(): void {
    window.removeEventListener('resize', this.updatePageSize)
  }

  private get styles(): object {
    return {
      '--window-width': `${this.state.pageSize.width}px`,
      '--window-height': `${this.state.pageSize.height}px`,
    }
  }

  private updatePageSize(): void {
    this.state.pageSize = {
      width: window.innerWidth,
      height: window.innerHeight,
    }
  }
}
</script>

<style lang="scss">
header {
  display: flex;
  align-items: center;
  height: 6rem;
  padding: 1rem 2rem;
  img {
    max-height: 100%;
  }
}
footer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 6rem;
}
</style>

<style lang="scss" scoped>
.chibi929-app-layout {
  font-size: 1.6rem;

  .page {
    width: 100%;
    height: auto;
    min-height: calc(var(--window-height) - 6rem);
  }
}
</style>

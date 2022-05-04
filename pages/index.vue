<template>
  <div class="index-page">
    <h1>IndexPage</h1>
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

<style lang="scss" scoped>
.index-page {
  h1 {
    color: $color_primary;
  }
}
</style>

<template>
  <div class="index-page">IndexPage</div>
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

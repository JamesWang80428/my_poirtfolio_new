<template>
  <div class="wrapper">
    <amp-img
      alt="home logo"
      src="/icon.svg"
      width="180"
      height="187"
      layout="fixed"
    />

    <type-label />
  </div>
</template>

<script>
import TypeLabel from '~/components/TypeLabel.vue'
import { metaHead } from '~/utils'

export default {
  name: 'AmpHome',
  layout: 'default.amp',
  components: { TypeLabel },
  head() {
    return {
      ...metaHead('Home 🏠', 'My Personal Website as a Developer. Here you can check my Resume'),
      link: [
        { rel: 'canonical', href: `${process.env.BASE_URL || ''}/` }
      ]
    }
  }
}
</script>

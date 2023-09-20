<template>
  <div class="container">
    <CardCharacter/>

  </div>
</template>

<script>

import CardCharacter from '../particles/CardCharacter.vue';

export default {
  name: 'SectionCharacters',
  components: {
		CardCharacter,
	}
}
</script>

<style lang='scss' scoped>

</style>
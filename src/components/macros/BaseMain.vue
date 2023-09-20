<template>
	<div class="container">
		<SectionCharacters/>
	</div>
</template>

<script>
import SectionCharacters from '../sections/SectionCharacters.vue';


export default {
	name: "BaseMain",
	components: {
		SectionCharacters,
	}
};
</script>

<style scoped lang="scss">

//MIXIN
@import '../../assets/style/mixins.scss';

.container {

}
</style>

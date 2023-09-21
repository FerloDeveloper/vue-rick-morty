<template>
	<div class="container">
		<h1>RICK e MORTY</h1>


	</div>
</template>

<script>
export default {
	name: "BaseHeader",
};
</script>

<style scoped lang="scss">
//MIXIN
@import "../../assets/style/mixins.scss";

.container {
	/* @include flex_center  */

	h1 {
		text-align: center;
	}

}

</style>

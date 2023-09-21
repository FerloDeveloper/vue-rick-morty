<template>
	<div class="container">
		<nav class="navbar navbar-light bg-light" @submit.prevent="$emit('searching', searchText)">
			<form class="form-inline">
				<input
					class="form-control mr-sm-2"
					type="search"
					placeholder="Search"
					aria-label="Search"
          v-model="searchText"
				/>
				<button class="btn btn-outline-success my-2 my-sm-0" type="submit">
					Search
				</button>
        <button type="button" class="btn btn-danger">Danger</button>
			</form>
		</nav>
	</div>
</template>

<script>
export default {
	name: "SearchBar",
  data() {
    return {

      searchText: "",
    }
  }
};
</script>

<style lang="scss" scoped></style>

<template>
	<div class="container">
		<div class="row">
			<div class="col-12">
				<SearchBar @searching="filterAlbum" />
			</div>
		</div>
		<div class="row">
			<CardCharacter
				class="col-12 col-sm-6 col-lg-3"
				v-for="character in AlbumFiltered"
				:key="character.id"
				:character="character"
			/>
		</div>
	</div>
</template>

<script>
import CardCharacter from "../particles/CardCharacter.vue";
import SearchBar from "../particles/SearchBar.vue";
import axios from "axios";

export default {
	name: "SectionCharacters",
	data() {
		return {
			characters: [],
			AlbumFiltered: [],
		};
	},
	created() {
		axios
			.get("https://rickandmortyapi.com/api/character")
			.then((response) => {
				// handle success
				console.log(response.data.results);
				this.characters = response.data.results;
				this.AlbumFiltered = response.data.results;
			})
			.catch((error) => {
				console.log(error);
			});
	},
	components: {
		CardCharacter,
		SearchBar,
	},
	methods: {
		filterAlbum(searchText) {
			this.AlbumFiltered = this.characters.filter((character) =>
				character.name.toLowerCase().includes(searchText.toLowerCase())
			);
		},
	},
};
</script>

<style lang="scss" scoped></style>

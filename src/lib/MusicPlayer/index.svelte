<script lang="ts">
	import { spring } from 'svelte/motion';

    const sampleObj = [{
        name: "Acousticbreeze",
        img_url: "/static/img/acousticbreeze.jpg",
        song_url: "bensound-acousticbreeze.mp3"
        }, 
        {
        name: "Buddy",
        img_url: "/static/img/buddy.jpg",
        song_url: "bensound-buddy.mp3"

        }, 
        {
        name: "Happyrock.jpg",
        img_url: "/static/img/happyrock.jpg",
        song_url: "bensound-happyrock.mp3"
        }, {
        name: "Memories",
        img_url: "/static/img/memories.jpg",
        song_url: "bensound-memories.mp3"

        }]

	let count = 0;

	const displayed_count = spring();
	$: displayed_count.set(count);
	$: offset = modulo($displayed_count, 1);

	function modulo(n: number, m: number) {
		// handle negative numbers
		return ((n % m) + m) % m;
	}
</script>

<div class="player-list">

hey I am a player

</div>

<style></style>

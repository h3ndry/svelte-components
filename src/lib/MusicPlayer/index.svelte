<script lang="ts">
	import { spring } from 'svelte/motion';

    import Player from './player.svelte';

    const songs = [{
        name: "Acousticbreeze",
        img: "/static/img/acousticbreeze.jpg",
        song_url: "/static/sound/bensound-acousticbreeze.mp3",
        id: 1
        }, 
        {
        name: "Buddy",
        img: "/static/img/buddy.jpg",
        song_url: "/static/sound/bensound-buddy.mp3",
        id: 2
        }, 
        {
        name: "Happyrock.jpg",
        img: "/static/img/happyrock.jpg",
        song_url: "/static/sound/bensound-happyrock.mp3",
        id: 3
        }, {
        name: "Memories",
        img: "/static/img/memories.jpg",
        song_url: "/static/sound/bensound-memories.mp3"

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
<div class="wrapper">
    
{#each songs as song (song.id)}

 <Player song={song!} />
 <img src={song.img} alt=""/>
{/each}


</div>
</div>

<style>



    .player-list {
        min-height: 29.375rem;
        padding: 4rem 0; }

    .wrapper{
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2rem 1rem;
        /* grid-column-gap: 1rem; */
        /* grid-row-gap: 2rem; */
        max-width: 65rem }

</style>

<script charset="utf-8">
  export let name;
  export let img;
  export let song_url;

  function play(el) {
	 el.play() 
  }

  function pause(el) {
	  el.pause()
  }

  function handleClick(event) {
	  el.pause()
  }


	
</script>

<div class="player">

	<div class="song-img">
		<img src={img} alt=""/>
	</div>

	<h3 class="song-name">{name}</h3>
	<h3 class="artist-name">artist name</h3>

	<span class="icon">I</span>
	<span class="icon">I</span>

	<figure on:click={handleClick} class="media-controller">

         <audio>
	 <track kind="captions" />
             <source
                src={song_url}
                type="audio/ogg"
                kind="caption"
             />
            Your browser does not support the audio element.
        </audio> 

	<svg
	   xmlns="http://www.w3.org/2000/svg"
	   viewBox="0 0 135 134.99999"
	   version="1.1"
	   id="svg8">
	  <defs
	     id="defs2">
	</defs>

	  <ellipse
	      class="ellipse"
	     cx="-67.499992"
	     cy="67.5"
	     rx="61.500046"
	     ry="61.50005"
	     transform="rotate(-90)" />
	  <g
	      class="pause"
	     transform="translate(-0.17777825,-0.18127833)">
	    <path
	       d="M 51.271205,42.984758 V 92.552532"
	       id="path1673" />
	    <path
	      class="pause"
	       d="M 84.08435,42.810016 V 92.37779"
	       id="path1673-6" />
	  </g>

	  <path
	      class="play"
	     transform="translate(5,0)"
	     d="m 86.259187,63.361495 -31.584,-22.646 c -3.369,-2.416 -8.059,-0.008 -8.059,4.138 v 45.293 c 0,4.146 4.69,6.554 8.059,4.138 l 31.583,-22.647 c 2.834,-2.031 2.834,-6.244 10e-4,-8.276 z" />

	  <ellipse
	      class="ellipse-overlay"
	     cx="-67.499992"
	     cy="67.5"
	     rx="61.500046"
	     ry="61.50005"
	     transform="rotate(-90)" />
	</svg>

	</figure>

</div>

<style>

    .player {

        display: grid;
        grid-template-columns: 8.25rem 1rem 2fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        grid-column-gap: 1.5rem;

        height: 8rem;
        padding: .8rem;
        border-radius: 10px;
        background: #282828 }
        
    .song-img {
        grid-column: 1 / 2;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;

        display: grid;
        justify-content: center;
        align-content: center;

        width: 8rem;
        height: 8rem;
        position: relative;
        border-radius: 15px;
        overflow: hidden;
        background: #222 }
    
    .song-img img {
        /* width: 110%; */
        /* transform: translateX(-5%); */
    }

    .song-image .overlay {
        position: absolute;
        width: 5.25rem;
        height: 5.25rem;
        opacity: .3;
        background: var(--bg-color-1)
    }

    .media-controller{
        grid-column: 4 / -1;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;
        margin: 0;
        padding: 0;

        display: grid;
        justify-content: center;
        align-content: center;

        border-radius: 50%;
        width: 4rem;
        height: 4rem; }
        /* background: var(--bg-color-1) } */
    
    .artist-name, .song-name {
        padding: 0;
        margin: 0;
        /* opacity: .8; */
        /* background-color: var(--bg-color-1); */
	text-transform: capitalize;
        grid-column: 2 / span 2;
     }

    .song-name {
        /* align-self: center; */
        align-self: end;
    }

    .artist-name {
        /* align-items: bottom; */
	font-weight: 400;
       }

    .icon {
        height: 1.5rem;
        width: 1.5rem;
        background-color: var(--bg-color-1);
        border-radius: 50%;
    }

    svg {
        width: 4rem;
        height: 4rem;
        cursor: pointer;
    }

    svg ellipse {
        display: inline;
        fill: none;
        stroke: orangered;
        stroke-width: 6;
        stroke-miterlimit: 4;
        /* stroke-opacity: .8; */

    }

    svg path.play {
        fill: orangered;
        fill-opacity: 1;
    }
    
    /* svg g.pause { */
    /* } */

    svg g.pause path {
        fill: none;
        display: none;
        stroke: orangered;
        stroke-width: 6;
        stroke-linecap: round;

    }

    svg path.show {
        fill-opacity: 1 !important;
        display: inline;
    }
    svg g.show path {
        display: inline;
    }

    svg .ellipse-overlay {
        stroke: orangered;
        /* opacity: 0; */
    }
    svg .ellipse {
        stroke: white;
        opacity: .5;
    }
    
</style>

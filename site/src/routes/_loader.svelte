<script>
    import {onMount} from "svelte";
	let isPageloaded=false;
	onMount(()=>{
            isPageloaded=true;
    });	
</script>

{#if !isPageloaded}
   <div class="loader"><img src="/Logo_ring.gif" alt=""></div>
{/if}
<slot />

<style>
.loader {
	position: fixed;
	background-color: black;
	width: 100vw;
	height: 100vh;
	z-index: 20;
    /* top:0;
    right:0;
    display: grid; */
}
img {
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
}

</style>
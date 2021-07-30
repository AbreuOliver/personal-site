<script>
    import { fly } from 'svelte/transition';
    export let show = false;
</script>

{#if show}
    <nav 
        transition:fly={{ y: -1550, opacity: 1 }}>
        <!-- <br>
        <br>
        <p>Close Menu</p> -->
    </nav>
{/if}


<style>
    nav {
        position: fixed;
        top: 0;
        right: 0;
        height: 50%;
        min-height: 500px;
        /* padding: 2rem 2rem 0.6rem; */
        background: #FFC300;
        overflow-y: auto;
        width: 100vw;
        min-width: 320px;
        color: #fff;
        font-weight: 400;

		/* display: flex; */
		/* justify-content: center; */
		/* max-width: 65ch; */
		margin: 0 auto;
		/* min-height: 50px; */
		/* height: 8vh; */
		/* max-height: 100px; */
		/* border: 1px solid dodgerblue; */
		padding: 0 5%;
		overflow: hidden;
    }

</style>






<!-- 
{#if show}
    <nav transition:fly={{x: 1550, 
        opacity: 1
        }}>
        <h2>Current Participant: <span>{$participantName}</span></h2>
        <h2>Participant Number: <span>#{$participantNumber}</span></h2>
        <br>
        <input bind:value={$participantName}>
        <br>
        <input bind:value={$participantNumber}><button on:click="{() => $participantNumber = ('')}">
            Reset Participant Number
        </button>
        <br>
        <button on:click="{() => $participantName = ('')}">
            Reset Participant Name
        </button>
        <br>
        <button>Go Back</button>
    </nav>
{/if} -->



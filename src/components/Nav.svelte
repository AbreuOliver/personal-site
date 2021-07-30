<script>
	import Sidebar from './Sidebar.svelte';
	let sidebar_show = false;
</script>

<div class="sticky">
	<nav>
		<div class="logo-area">
			<a href=".">Oliver Abreu</a>
		</div>
		<div class="menu">
			<!-- <a href="about">about</a>
			<a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a> -->
			<span 
				class="hamburger"
				on:click={() => sidebar_show = !sidebar_show} 
			>
				<span class="stick stick-1 hover"></span>
				<span class="stick stick-2 hover"></span>
			</span>
		</div>
		<Sidebar bind:show={sidebar_show} />
	</nav>
</div>


<style>
	:global(.noscroll) {
		overflow: hidden;
	}
	nav {
		font-weight: 300;
		display: flex;
		align-items: center;
		max-width: 65ch;
		margin: 0 auto;
		min-height: 50px;
		height: 8vh;
		max-height: 100px;
		/* border: 1px solid dodgerblue; */
		padding: 0 5%;
		overflow: hidden;
	}
	.logo-area {
		flex: 1;
		overflow-y: hidden;
		z-index: 100;
		/* border: 1px solid pink; */
	}
	.logo-area a:hover {
		color: #FFC300;
	}
	a {
		text-decoration: none;
		display: block;
		text-transform: uppercase;
		display: block;
		float: left;
		font-size: 16px;
		color: #3D3D3D;
		overflow-y: hidden;
	}
	.menu {
		z-index: 100;
	}
	.hamburger{
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: flex-end;
		cursor: pointer;
		/* border: 1px solid green; */
	}

	.hamburger:hover .hover {
		background: #FFC300;
	}

	.hamburger:active .hover {
		background: #FFC300;
	}

	.stick {
		display: inline-block;
		background-color: #3d3d3d;
		height: 3px;
		border-radius: 5px;
	}

	.stick-1 {
		width: 40px;
		margin-bottom: 5px;
		
	}

	.stick-2 {
		width: 30px;
	}

	.sticky {
		position: -webkit-sticky;
		background: #fff;
		position: sticky;
		top: 0;
		z-index: 100;
	}
</style>

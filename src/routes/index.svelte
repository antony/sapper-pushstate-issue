<h1>
	Page One.
</h1>

<button on:click={addParam}>add state with query</button>

<button on:click={gotoAbout}>go to about page</button>

<script>
	import { goto } from '@sapper/app'

	function gotoAbout () {
		goto('/about')
	}

	function addParam () {
		history.pushState(null, null, '/?foo=bar')
	}
</script>
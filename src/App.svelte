<script>
    let name=''
    let author=''

	let songs=[
		{
			name:'Good Vibe',
			author:'Jfla'
		},
		{
			name:'Different World',
			author:'Alan Walker'
		},
		{
			name:'City of Stars',
			author:'La La Land'
		},
		{
			name:'High Hopes',
			author:'Panic! At The Disco'
		}
	]

	function clearInputs(){
		name=''
		author=''
	}

	function addSongList(){
		songs=[...songs, {name:name, author:author}]
		clearInputs()
	}
</script>
<div class="container">
	<ul class="list-group">
		{#each songs as song}
			<li class="list-group-item">{song.name}
			<b class="float-right">{song.author}</b></li>
		{/each}
	</ul>

	<form class="mt-2" on:submit|preventDefault={addSongList}>
		<input type="text" class="form-control" bind:value={name} placeholder="Song Name">
		<input type="text" class="form-control" bind:value={author} placeholder="Author">
		<button class="btn btn-outline-primary btn-block" disabled={name==''|author==''}>Add</button>
	</form>
</div>

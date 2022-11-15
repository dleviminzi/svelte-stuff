<script>
	let lessons = [
		{ lessonName: 'class 1', lessonDescription: 'do first stuff' },
		{ lessonName: 'class 2', lessonDescription: 'then do more stuff' },
		{ lessonName: 'class 3', lessonDescription: 'move on to the new stuff' }
	];

	function add() {
		lessons = lessons.concat({ lessonName: '', lessonDescription: '' });
	}
</script>

<h1>Lessons</h1>

<div class="flex overflow-x-auto space-x-8 w-3/4">
	{#each lessons as lesson}
		<div>
			<input placeholder="give this lesson a title" bind:value={lesson.lessonName} />
			<input placeholder="give this lesson a description" bind:value={lesson.lessonDescription} />
		</div>
	{/each}

	<button on:click={add}> Add new lesson to week </button>
</div>

<script>
	const data = { content: 'hello', lang: 'js' };
</script>

<div>
	{#if data.lang}
		<span class="lang">{data.lang}</span>
	{/if}
</div>
<div>{@html data.content}</div>

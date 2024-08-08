<script>
	const data = { content: 'hello', lang: 'js', start: '```', end: '```' };
</script>

{#if data}
	<div class="code-block" spellcheck="false">
		<div class="line">
			<span class="symbol">{data.start}</span>{#if data.lang}<span class="lang">{data.lang}</span
				>{/if}
		</div>
		{#if data.content}{#each data.content.split('\n') as line}<div class="line">
					{@html line}
				</div>{/each}{/if}{#if data.end}<div class="line">
				<span class="symbol">{data.end}</span>
			</div>
		{/if}
	</div>
{/if}

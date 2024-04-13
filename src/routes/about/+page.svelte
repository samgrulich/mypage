<script lang="ts">
	import Card from "$lib/components/card.svelte";
</script>

<style>
    ul {
        list-style-type: none;
        padding: 0;
    }
</style>

<h2>Hallo mallo</h2>
<ul>
<li><Card name="no">FU</Card></li>
<li><Card name="yes">Yipee</Card></li>
<li><Card name="maybe">Oh no</Card></li>
<li><Card>No text :(</Card></li>
</ul>

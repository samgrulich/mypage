<script lang="ts">
	import Card from "$lib/components/card.svelte";

</script>

<style>
    .centered {
        text-align: center;
        padding: 30vh 0;
    }
    .greeting {
        font-size: 4rem;
    }
    ul {
        list-style-type: none;
    }
    li {
        display: inline;
    }
</style>

<div class="centered" style:color="#fff">
    <h1 class="greeting">Welcome</h1>
</div>
<ul>
    <li><Card name="Projects" href="/projects">FU</Card></li>
    <li><Card name="About me" href="/about">Yipee</Card></li>
</ul>

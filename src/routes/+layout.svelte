<script>
	import Badge from "$lib/components/badge.svelte";
	import GithubBadge from "$lib/components/badges/githubBadge.svelte";

</script>
<svelte:head>
    <title>Home</title>
    <meta name="description" content="Home page of the portfolio" />
</svelte:head>

<style>
    footer {
        text-align: center;
        padding: 1rem;
    }
    .menuNav {
        display: flex;
        justify-content: center;
    }
    .menuUL {
        list-style: none;
        display: flex;
        gap: 1rem;
    }
    .menuItem {
        padding: 0.5rem 1rem;
        border-radius: 3rem;
        background-color: #f0f0f0;
    }
    .menuItem a {
        text-decoration: none;
        color: #000;
    }
    .menuItem a:hover {
        text-decoration: underline;
    }
    .slotContainer {
        padding: 1rem;
    }
</style>

<header>
    <nav class="menuNav">
        <ul class="menuUL">
            <li class="menuItem"><a href="/">Home</a></li>
            <li class="menuItem"><a href="/projects">Projects</a></li>
            <li class="menuItem"><a href="/about">About</a></li>
        </ul>
    </nav>
</header>

<div class="slotContainer">
    <slot />
</div>

<footer>
    <hr/>
    <p>Footer</p>
    <GithubBadge href="https://github.com/samgrulich"></GithubBadge>
</footer>

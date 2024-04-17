<script>
	import Badge from "$lib/components/badge.svelte";
	import GithubBadge from "$lib/components/badges/githubBadge.svelte";
	import MailBadge from "$lib/components/badges/mailBadge.svelte";

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
        min-height: 80vh;
    }
    footer {
        background-color: #fff;
        border-radius: 3rem 3rem 0 0;
        padding: 2rem;
        display: flex;
        justify-content: center;
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
    <GithubBadge href="https://github.com/samgrulich" size={60}></GithubBadge>
    <MailBadge size={60}></MailBadge>
</footer>

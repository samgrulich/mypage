<script>
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
        padding: 6rem 0 0 0;
        min-height: 80vh;
    }
    footer {
        /* background-color: #fff; */
        border-radius: 3rem 3rem 0 0;
        padding: 2rem;
        display: flex;
        justify-content: center;
    }
    .masterWrapper {
        background-color: #7ab9f4;
        padding: 1rem 0 0 0;
        background: radial-gradient(ellipse at top,    rgba(202,185,244,1) 0%, rgba(60,212,255,0) 100%),
                    radial-gradient(ellipse at bottom, rgba(202,185,244,1) 0%, rgba(60,212,255,0) 100%);
    }
    a {
        transition: all ease-in-out 0.1s;
    }
    li:hover a {
        color: rgba(0, 200, 200, 0.7);
    }
    .footerBadges {
        display: flex;
        gap: 1rem;
    }
</style>

<div class="masterWrapper">
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
<div class="footerBadges">
    <GithubBadge href="https://github.com/samgrulich" size={60}></GithubBadge>
    <MailBadge to="sam@supergrulisi.cz" size={60}></MailBadge>
</div>
</footer>
</div>

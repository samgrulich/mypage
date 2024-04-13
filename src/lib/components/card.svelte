<script lang="ts">
    export let name: string = "Unknown";
    export let href: string|undefined = undefined;
</script>

<style>
    div {
        padding: 1em;
        margin: 1em;
    }
    h1 {
        color: #fff;
    }
    a {
        text-decoration: none;
        color: #000;
    }
    .root {
        border: 1px solid #000;
        border-radius: 3rem;
        padding: 2rem;
        margin: 2rem auto 2rem auto;
        max-width: 600px;

         /* From https://css.glass */
        background: rgba(255, 255, 255, 0.6);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(6.1px);
        -webkit-backdrop-filter: blur(6.1px);
        border: 1px solid rgba(255, 255, 255, 0.3);   min-width: 200px;
    }
    .slotContainer {
        border-radius: 3rem;
        padding: 3rem;
        background-color: white;
        box-shadow: 0 30px 30px rgba(255, 255, 255, 0.3);
        min-height: 50px;
    }
</style>

<a {href}>
<div class="root">
    <h1>{name}</h1>
    <div class="slotContainer"><slot/></div>
</div>
</a>

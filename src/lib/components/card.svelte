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
        color: rgba(0, 0, 0, 0.7);
    }
    a {
        text-decoration: none;
        color: #000;
        margin: 2rem auto 2rem auto;
        padding: 0;
        display: inline-flex;
    }
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0;
        padding: 0;
    }
    .innerContainer {
        border: 1px solid #000;
        border-radius: 3rem;
        max-width: 600px;
        padding: 2rem;
        margin: 0;

         /* From https://css.glass */
        background: rgba(255, 255, 255, 0.6);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(6.1px);
        -webkit-backdrop-filter: blur(6.1px);
        border: 1px solid rgba(255, 255, 255, 0.3);   
        min-width: 200px;

        transition: all ease-in-out 0.2s;
    }
    .innerContainer:hover {
        scale: 1.01;
    }
    .slotContainer {
        display: flex;
        border-radius: 3rem;
        padding: 2rem;
        background-color: white;
        box-shadow: 0 30px 30px rgba(255, 255, 255, 0.3);
        min-height: 50px;
        position: relative;

        transition: all ease-in-out 0.2s;
    }
    .imgContainer {
        position: relative;
        width: 100px;
        height: 100px;
        margin: auto 0;
    }
    .innerContainer:hover .slotContainer {
        scale: 1.03;
    }
    .childrenContainer {
        padding: 0;
        margin: 0;
        width: 100%;
        width: 300px;
    }
    @media (max-width: 600px) {
        .imgContainer {
            display: none;
        }
        .childrenContainer {
            margin: auto;
        }
    }
</style>

<div class="container">
<a {href}>
<div class="innerContainer">
    <h1>{name}</h1>
    <div class="slotContainer">
    <div class="imgContainer">
    <slot name="imgs" />
    </div>
    <div class="childrenContainer">
    <slot />
    </div>
    </div>
</div>
</a>
</div>

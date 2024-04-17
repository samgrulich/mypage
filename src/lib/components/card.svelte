<script lang="ts">
    export let name: string = "Unknown";
    export let href: string|undefined = undefined;
    let isHovered = false;
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

        transition: all ease-in-out 0.2s;
    }
    .root:hover {
        scale: 1.01;
    }
    .slotContainer {
        display: flex;
        border-radius: 3rem;
        padding: 3rem;
        background-color: white;
        box-shadow: 0 30px 30px rgba(255, 255, 255, 0.3);
        min-height: 50px;

        transition: all ease-in-out 0.2s;
    }
    .imgContainer {
        position: relative;
        width: 100px;
        height: 100px;
    }
    .root:hover .slotContainer {
        scale: 1.03;
    }
</style>

<a {href}>
<div class="root">
    <h1>{name}</h1>
    <div class="slotContainer">
    <div class="imgContainer">
        <img style="position: absolute; top: -10px; left: 15px; border-radius: 50%" src="https://i.pinimg.com/736x/91/09/79/910979a5f0722da3fccb2e1032dc3100.jpg" alt="" width=60px>
        <img style="position: absolute; top: 45px; left: 80px;  border-radius: 50%" src="https://i.kym-cdn.com/entries/icons/facebook/000/021/807/ig9OoyenpxqdCQyABmOQBZDI0duHk2QZZmWg2Hxd4ro.jpg" alt="" width=40px height=40px>
        <img style="position: absolute; top: 70px; left: 10px;  border-radius: 50%" src="https://i.ytimg.com/vi/KEkrWRHCDQU/maxresdefault.jpg" alt="" width=50px height=50px>
    </div>
    <slot/>
    </div>
</div>
</a>

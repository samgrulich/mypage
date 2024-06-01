<script lang="ts">
    import { onMount } from "svelte";
    export let speed: number = 10;
    export let style: string = "";

    let shadowPos: number, start: number, width: number, xPos: number, stopPos: number;
    let id: number = Math.floor(Math.random() * Number.MAX_SAFE_INTEGER);
    
    onMount(() => {
        const slot = document.querySelectorAll(`#slot-${id}`);

        start = -1 * slot[0].getBoundingClientRect().width - 100;
        stopPos = window.innerWidth;
        width = slot[0].getBoundingClientRect().width;
        xPos = 0;
        shadowPos = start;

        setInterval(() => {
            if (speed > 0) {
                xPos = (xPos + speed);
                shadowPos = (shadowPos + speed);
                if (xPos > stopPos) {
                    xPos = start + shadowPos;
                }
                if (shadowPos > stopPos) {
                    shadowPos = start + xPos;
                }
            } else {
                xPos = (xPos + speed);
                shadowPos = (shadowPos + speed);
                if (xPos < start) {
                    xPos = window.innerWidth + (width - window.innerWidth) + 100;
                }
                if (shadowPos < start) {
                    shadowPos = window.innerWidth + (width - window.innerWidth) + 100;
                }
            }
        }, 16);
    });
</script>

<style>
    .slot{
        position: absolute; 
        display: flex;
        gap: 100px;
        margin: 0;
        padding: 0;
        left: 0;
    }

    .container {
        position: relative;
        overflow: hidden;
        width: 100%;
        height: 3.5rem;
        background-color: rgba(0, 155, 255, 0.2);
        box-shadow: 0 3px 10px rgba(255, 255, 255, 0.1);
        padding-top: 0.5rem;
    }

    @media (max-width: 600px) {
        .container {
            visibility: hidden;
        }
    }
</style>


<div style="{style}" class="container">
<div id="slot-{id}" class="slot" style="left: {xPos}px"> 
    <slot />
</div>
<div id="shadow-{id}" class="slot" style="left: {shadowPos}px"> 
    <slot />
</div>
</div>

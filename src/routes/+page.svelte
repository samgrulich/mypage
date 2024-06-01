<script lang="ts">
	import Card from "$lib/components/card.svelte";
	import Carousel from "$lib/components/carousel.svelte";
</script>

<style>
    .centered {
        text-align: center;
        margin: 16vh 0 62vh 0;
    }
    .greeting {
        font-size: 4rem;
        z-index: 30;
        position: relative;
    }
    .button {
        width: 100%;
        height: 100%;
        font-size: 2.2rem;
        color: #2c2959;
        font-weight: 600;
        align-content: end;
        text-align: right;
    }
    .arrow {
        opacity: 0.4;
    }
    .wordle {
        width: 100vw;
        height: 100vh;
        position: absolute;
        z-index: 20;
        top: 0;
        left: 0;
        color: #fff;
        font-size: 3rem;
        font-weight: 600;
        /* overflow: hidden; */
    }
    ul {
        list-style-type: none;
        padding: 0;
        z-index: 30;
        position: relative;
    }
    li {
        display: flex;
        justify-content: center;
    }
    @media (max-width: 600px) {
        .centered {
            margin: 0vh 0 10vh 0;
        }
        .greeting {
            font-size: 2.5rem;
        }
        .button {
            font-size: 1.5rem;
        }
    }
</style>

<div class="centered" style:color="#2c2959">
    <!-- <div><h1 class="greeting">Hola!</h1></div> -->
    <!-- <div><h1 class="greeting">Salut!</h1></div> -->
    <!-- <div><h1 class="greeting">Ahoj!</h1></div> -->
    <!-- <div><h1 class="greeting">Salut!</h1></div> -->
    <div><h1 class="greeting">sup</h1></div>

    <div class="wordle">
        <Carousel style="top: 68vh" speed={2.1}>
            <div>C--</div>
            <div>C</div>
            <div>Rust</div>
            <div>Svelte</div>
            <div>Python</div>
            <div>Neovim</div>
            <div>Linux</div>
            <div style="width: 300px;">Arch, btw</div>
        </Carousel>

        <Carousel style="top: 72vh" speed={-4.2}>
            <span>NextJS</span>
            <span>React</span>
            <span>TS</span>
            <span>JS</span>
            <span>Go</span>
            <span>C#</span>
            <span>Java</span>
            <span>OpenGL</span>
            <span>PHP</span>
            <span>Homelab</span>
        </Carousel>
    </div>
</div>
<ul>
    <li><Card name="Projects" href="/projects">
      <div class="button">Let's see <span class="arrow">-></span></div>
    </Card></li>
    <li><Card name="About me" href="/about">
      <div class="button">Check it out <span class="arrow">-></span></div>
    </Card></li>
</ul>

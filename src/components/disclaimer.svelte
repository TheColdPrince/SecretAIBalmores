<script>
    export let close;
    import { slide } from "svelte/transition";
</script>

<main transition:slide={{ duration: 128 }}>
    <h4 class="text-center" style="margin-bottom: .75rem;">Important!</h4>
    <p class="text-center" style="line-height: 190%;">
We will now shut down this application by MegaFlash XYZ in the following months; this application is too expensive to maintain, intendedly planned for two months only.    <hr />
    <button on:click={close}> I understand </button>
</main>

<style>
    button:hover {
        background-color: hsla(0, 0%, 100%, 0.1);
    }
    button:active {
        background-color: hsla(0, 0%, 100%, 0.2);
    }
    button {
        cursor: pointer;
        background-color: transparent;
        color: dodgerblue !important;
        width: 100%;
        text-align: center;
        border-radius: 0.3rem;
        font-size: 0.8rem;
        font-weight: 600;
        transition: 100ms;
    }
    hr {
        opacity: 0.1;
        margin: 1rem 0;
    }
    main {
        background: linear-gradient(
            135deg,
            hsl(235, 92%, 5%),
            hsl(326, 92%, 5%)
        );
        backdrop-filter: blur(30px);
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 10;
        border: 1px solid hsla(0, 0%, 100%, 0.5);
        border-radius: 9px;
        width: min(500px, 80vw);
        font-size: 0.9rem;
        overflow: hidden;
        padding: 1.5rem;
    }
</style>

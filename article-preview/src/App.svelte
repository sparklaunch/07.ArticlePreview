<script lang="ts">
    import Card from "./components/Card.svelte";
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
        href="https://fonts.googleapis.com/css2?family=Manrope:wght@500;700&display=swap"
        rel="stylesheet"
    />
    <style>
        body {
            background-color: rgb(234, 240, 247);
        }
    </style>
</svelte:head>
<div id="app">
    <Card />
</div>

<style>
    #app {
        width: 100vw;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    @media all and (max-width: 1440px) {
        #app {
            padding: 100px 0;
            display: block;
            height: auto;
            width: 100%;
        }
    }
</style>

<script lang="ts">
    import Texts from "./Texts.svelte";
    import Profile from "./Profile.svelte";
</script>

<div id="right">
    <Texts />
    <Profile />
</div>

<style>
    #right {
        padding: 40px;
        background-color: white;
        border-top-right-radius: 10px;
        border-bottom-right-radius: 10px;
    }
</style>

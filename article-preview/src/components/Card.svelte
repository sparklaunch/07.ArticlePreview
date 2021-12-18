<script lang="ts">
    import Left from "./Left.svelte";
    import Right from "./Right.svelte";
</script>

<div id="card">
    <Left />
    <Right />
</div>

<style>
    #card {
        border-radius: 10px;
        box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.25);
        display: flex;
        align-items: stretch;
        width: 60%;
    }
</style>

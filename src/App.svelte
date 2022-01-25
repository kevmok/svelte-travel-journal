<script>
    import data from './data';
    import Navbar from './components/navbar.svelte';
    import Main from './components/Main.svelte';
</script>

<div>
    <Navbar />
    {#each data as item}
        <Main {...item} />
    {/each}
</div>

<style>
    :global(body) {
        margin: 0;
        padding: 0;
        font-family: 'Inter', sans-serif;
    }
</style>

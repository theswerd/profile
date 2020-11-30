<script>
    export let title;
    export let technologies;
    export let projects;
    export let recommendations;
</script>

<style>
    column {
        text-align: center;
    }
    li {
        list-style: none;

    }
    ul {
        padding: 0px;
        margin: 0px;
        font-size: 25px;
    }
    h1 {
        font-size: 36px;
        padding: 0px;
        margin: 0px;
    }
    h2 {
        padding: 10px;
        margin: 0px;
    }
   
</style>

<column>
    <h1>{title}</h1>
    {#if technologies != undefined}
        <h2>Technologies</h2>
        <ul>
            {#each technologies as technology}
                <li>{technology}</li>
            {/each}
        </ul>
    {/if}

    {#if projects != undefined}
        <h2>Projects</h2>
        <ul>
            {#each projects as project}
                <li>{@html project}</li>
            {/each}
        </ul>
    {/if}
    {#if recommendations != undefined}
        <h2>Recommendations</h2>
        <ul>
            {#each recommendations as recommendation}
                <li>{recommendation}</li>
            {/each}
        </ul>
    {/if}
</column>

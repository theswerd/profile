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
        padding: 0px 0px 0px 5px;

    }
    ul {
        margin: 0px;
        padding: 0px;
        font-size: 25px;
    }
    h1 {
        font-size: 40px;
        padding: 5px;
        margin: 0px;
    }
    h2 {
        padding: 10px;
        font-size: 30px;
        margin: 0px;
    }
   column {
       padding-bottom: 25px;
   }
   a:hover {
       color: #ffaaaa;
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
        <li><a href={project.link}>{project.name}</a></li>
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

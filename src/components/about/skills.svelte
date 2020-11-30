<script>
const { default: SkillsContainer }=require("./skillsContainer.svelte");

</script>

<style>
    .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, 300px);
        justify-content: center;
    }
    section {
        padding-left: 20px;
    }
    h1 {
        font-size: 40px;
    }
</style>

<section>
    <h1>Skills</h1>
    <div class="grid">
        <SkillsContainer title="Mobile" technologies={["Flutter", "Dart"]} projects={["<a href='https://github.com/worldhealthorganization/app'>World Health Organization App</a>"]}></SkillsContainer>
        <SkillsContainer title="Web"></SkillsContainer>
        <SkillsContainer title="Cloud"></SkillsContainer>
        <SkillsContainer title="Management"></SkillsContainer>

    </div>
</section>

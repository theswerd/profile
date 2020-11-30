<script>
    import SkillsContainer from "./skillsContainer.svelte";

    let mobileTechnologies = [
        "Flutter",
        "Dart",
        "Hybrid Native Apps",
        "Android",
        "iOS",
    ];
    let mobileProjects = [
        {
            link: "https://github.com/worldhealthorganization/app",
            name: "World Health Organization App",
        },
        {
            link: "https://github.com/theswerd/flutter_custom_license_page",
            name: "Flutter Custom License Page",
        },
        {
            link: "https://github.com/theswerd/beachy",
            name: "Beachy App - Hack SC 2020",
        },
    ];

    let webTechnologies = [
        "JavaScript",
        "TypeScript",
        "Svelte",
        "Sapper",
        "ReactJS",
    ];
    let webProjects = [
        {
            link: "https://github.com/splashhacks/web",
            name: "Splash Hacks",
        },
        {
            link: "https://github.com/Public-Tree-Map/public-tree-map",
            name: "Public Tree Map",
        },
        {
            link: "https://github.com/theswerd/chemistry",
            name: "Chem.land",
        },
    ];

    let cloudTechnologies = [
        "Amazon Web Services",
        "Google Cloud Platform",
        "Vercel",
        "Github Pages",
        "Terraform",
        "Docker",
    ];
    

    let backendTechnologies = [
        "NodeJS",
        "ExpressJS",
        "Rust",
        "Rocket",
        "Actix",
    ];
    let databaseTechnologies = [
        "PostgreSQL",
        "AWS Aurora",
        "Hasura GraphQL",
        "Redis",
        "Cloud Firestore",
        "MongoDB"
    ];
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
        <SkillsContainer
            title="Mobile"
            technologies={mobileTechnologies}
            projects={mobileProjects} />
        <SkillsContainer
            title="Web"
            technologies={webTechnologies}
            projects={webProjects} />
        <SkillsContainer title="Cloud" 
        technologies={cloudTechnologies}/>
        <SkillsContainer title="Backend" 
        technologies={backendTechnologies}/>
        <SkillsContainer title="Database" 
        technologies={databaseTechnologies}/>
        <SkillsContainer title="Management" />
    </div>
</section>

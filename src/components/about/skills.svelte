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
        "SSR",
        "PWA",
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
        "Firebase",
        "Vercel",
        "Github Pages",
        "Github Actions",
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
    let backendProjects = [
        {
            link: "https://github.com/theswerd/beachy",
            name: "Beachy App - Hack SC 2020",
        },
    ];

    let databaseTechnologies = [
        "PostgreSQL",
        "AWS Aurora",
        "Hasura GraphQL",
        "Redis",
        "Cloud Firestore",
        "MongoDB",
    ];

    let managementProjects = [
        {
            link: "https://github.com/worldhealthorganization/app",
            name:
                "World Health Organization App Client UI Lead, Code Owner, and Technical Lead",
        },
    ];
    let innerWidth;
    $: outlined = innerWidth >= 900;
</script>

<style>
    .grid {
        display: grid;
        justify-content: center;
    }
    @media only screen and (max-width: 899px) {
        .grid {
            grid-template-columns: repeat(auto-fit, 300px);
        }
    }
    @media only screen and (min-width: 900px) {
        .grid {
            grid-template-columns: repeat(3, 1fr);
        }
    }

    section {
        padding: 0px 15px;
        border-bottom: 1px solid var(--accent);

    }
    h1 {
        font-size: 40px;
        margin-top: 5px;
        padding: 0px;
    }
</style>

<svelte:window bind:innerWidth />
<section>
    <h1>Skills</h1>
    <div class="grid">
        <SkillsContainer
            title="Mobile"
            technologies={mobileTechnologies}
            projects={mobileProjects}
            {outlined} />
        <SkillsContainer
            title="Web"
            technologies={webTechnologies}
            projects={webProjects}
            {outlined} />
        <SkillsContainer title="Cloud" technologies={cloudTechnologies} />
        <SkillsContainer
            title="Backend"
            technologies={backendTechnologies}
            projects={backendProjects}
            {outlined} />
        <SkillsContainer
            title="Database"
            technologies={databaseTechnologies}
            {outlined} />
        <SkillsContainer title="Management" projects={managementProjects} />
    </div>
</section>

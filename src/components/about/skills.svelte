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
    grid {
        display: grid;
        justify-content: center;
        border-bottom: 1px solid var(--accent);
    }
    technologiesGrid {
        display: grid;
        grid-template-columns: repeat(auto-fit, 75px);
        justify-content: center;
    }
    technologiesGrid img {
        margin: 15px;
    }
    @media only screen and (max-width: 899px) {
        grid {
            grid-template-columns: repeat(auto-fit, 300px);
        }
    }
    @media only screen and (min-width: 900px) {
        grid {
            grid-template-columns: repeat(3, 1fr);
        }
    }

    section {
        padding: 0px;
        margin: 0px;
        border-bottom: 1px solid var(--accent);
    }
    h1 {
        font-size: 40px;
        margin-top: 5px;
        padding: 15px;
    }
</style>

<svelte:window bind:innerWidth />
<section>
    <h1>Skills</h1>
    <grid>
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
    </grid>
    <technologiesGrid>
        <img src="tech/amazonaws.svg" alt="AWS" />
        <img src="tech/googlecloud.svg" alt="GCP" />
        <img src="tech/vercel.svg" alt="Vercel" />
        <img src="tech/firebase.svg" alt="Firebase" />
        <img src="tech/lambda.svg" alt="Lambda" />
        <img src="tech/docker.svg" alt="Docker" />
        <img src="tech/kubernetes.svg" alt="Kubernetes" />
        <img src="tech/ubuntu.svg" alt="Ubuntu" />
        <img src="tech/terraform.svg" alt="Terraform" />
        <img src="tech/node-dot-js.svg" alt="NodeJS" />
        <img src="tech/rust.svg" alt="Rust" />
        <img src="tech/python.svg" alt="Python" />
        <img src="tech/nginx.svg" alt="Nginx" />
        <img src="tech/redis.svg" alt="Redis" />
        <img src="tech/postgresql.svg" alt="PostgreSQL" />
        <img src="tech/graphql.svg" alt="GraphQL" />
        <img src="tech/flutter.svg" alt="Flutter" />
        <img src="tech/dart.svg" alt="Dart" />
        <img src="tech/git.svg" alt="Git" />
        <img src="tech/githubactions.svg" alt="Github Actions" />
        <img src="tech/jenkins.svg" alt="Jenkins" />
        <img src="tech/javascript.svg" alt="JavaScript" />
        <img src="tech/typescript.svg" alt="TypeScript" />
        <img src="tech/css3.svg" alt="CSS" />
        <img src="tech/react.svg" alt="React" />
        <img src="tech/next-dot-js.svg" alt="NextJS" />
        <img src="tech/vue-dot-js.svg" alt="VueJS" />
        <img src="tech/svelte.svg" alt="Svelte" />
        <img src="tech/socket-dot-io.svg" alt="SocketIO" />
        <img src="tech/yarn.svg" alt="Yarn" />
        <img src="tech/markdown.svg" alt="Markdown" />
        <img src="tech/stripe.svg" alt="Stripe" />
    </technologiesGrid>
</section>

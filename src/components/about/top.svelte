<script>
    let projects = [
        {
            name: "Public Tree Map",
            technologies: ["JavaScript", "CSS", "HTML", "Leaflet Maps"],
            description: "Public Tree Map was my first project at Hack For LA.",
            image: "projects/publictreemap.png",
        },
        {
            name: "WHO App",
            technologies: [
                "Dart",
                "Flutter",
                "Java",
                "Terraform",
                "GCP",
                "Google Analytics",
            ],
            description:
                "The WHO App team was the highest performance team I have ever worked on.",
            image: "projects/who.png",
        },
    ];

    let index = 0;

    let currentProject = projects[0];

    function setCurrentProject() {
        if (projects.length - 1 == index) {
            index = 0;
        } else {
            index++;
        }
        currentProject = projects[index];
    }
    setInterval(setCurrentProject, 8000);
</script>

<style>
    section {
        border-bottom: 1px solid var(--accent);
    }
    h1 {
        text-transform: uppercase;
        font-size: 100px;
        font-weight: 500;
        padding: 0px 0px;
        margin: 0px;
        white-space: nowrap;
    }

    p {
        margin-top: 5px;
        padding-left: 25px;
        padding-right: 25px;
        font-size: 16px;
        text-align: right;
    }

    h2 {
        padding-top: 0px;
        margin-bottom: 5px;
        margin-top: 5px;

        padding-left: 25px;
        text-transform: uppercase;
    }

    skills {
        -webkit-transform: rotate(-90deg);
        -moz-transform: rotate(-90deg);
        -o-transform: rotate(-90deg);
        -ms-transform: rotate(-90deg);
        transform: rotate(-90deg);
        float: left;
        position: absolute;
        justify-content: end;
        padding-left: 60px;
        margin-left: 20px;
        bottom: -40px;
    }

    section {
        height: calc(100vh - var(--nav-height));
        display: flex;
        align-items: flex-start;
    }
    @media only screen and (min-width: 501px) {
        skills {
            display: block;
        }
    }
    @media only screen and (max-width: 500px) {
        skills {
            display: none;
        }
    }

    @media only screen and (max-width: 1000px) {
        .desktopSidebar {
            display: none;
        }
    }
    @media only screen and (min-width: 1000px) {
        .adaptableSize {
            width: 600px;
        }
    }

    .desktopSidebar {
        border-left: 1px solid var(--accent);
        width: 100%;
        height: calc(100vh - var(--nav-height));
        transition: 400ms;
    }
    .imageContainer {
        background-color: var(--dark-grey);
        height: 400px;
        width: 100%;
    }
    .imageContainer img {
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
</style>

<section>
    <div>
        <div class="adaptableSize">
            <h2>I am an Aspiring Computer Scientist and tech lead</h2>
            <p>
                I've developed for and managed teams at organizations ranging
                from the community organization Hack for LA, to the World Health
                Organization. I'm fluent in the languages JavaScript,
                TypeScript, CSS, HTML, Rust, Dart, Python, SQL, GraphQL and
                Rust. I have worked with MariaDB, MySQL, PostgreSQL, AWS
                DynamoDB, Cloud Firestore, and MongoDB. I'm fluent in the
                frameworks React, Svelte, Flutter, Node, Express, Docker and
                many more. I also have experience developing on AWS, GCP,
                Vercel, and Github Pages.
            </p>

            <skills>
                <h1>Leader</h1>
                <h1>Mobile</h1>
                <h1>Cloud</h1>
                <h1>Web</h1>
            </skills>
        </div>
    </div>
    <div class="desktopSidebar">
        <div class="imageContainer">
            <img alt="" src={currentProject['image']} />
            <h2>{currentProject['name']}</h2>
            <p>{currentProject['description']}</p>
        </div>
    </div>
</section>

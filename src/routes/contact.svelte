<style>
    h2 {
        margin: 20px;
    }
    grid {
        display: grid;
        justify-content: center;
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
    contact {
        text-align: center;
        padding: 15px;
    }
    contact a {
        text-align: center;
    }
    contact img {
        height: 90px;
        margin: 0px;
        padding: 0px;
    }
    contact h3 {
        font-size: 25px;
        margin: 5px;
        padding: 0px;
    }
</style>

<svelte:head>
    <title>Contact</title>
</svelte:head>
<h2>I respond to messages on any of these platforms</h2>
<grid>
    <contact>
        <a href="https://www.instagram.com/ben_swerdlow/" target="_blank">
            <img src="socials/instagram.svg" alt="Instagram" />
            <h3>@ben_swerdlow</h3>
        </a>
    </contact>
    <contact>
        <a href="https://www.linkedin.com/in/benswerdlow/" target="_blank">
            <img src="socials/linkedin.svg" alt="LinkedIn" />
            <h3>/in/benswerdlow</h3>
        </a>
    </contact>
    <contact>
        <a href="https://twitter.com/benswerd" target="_blank">
            <img src="socials/twitter.svg" alt="Twitter" />
            <h3>@benswerd</h3>
        </a>
    </contact>
    <contact>
        <a href="https://www.facebook.com/swerdlowben/" target="_blank">
            <img src="socials/facebook.svg" alt="Facebook" />
            <h3>swerdlowben</h3>
        </a>
    </contact>
    <contact>
        <a href="mailto:swerdlowbenjamin@gmail.com" target="_blank">
            <img src="socials/gmail.svg" alt="Gmail" />
            <h3>swerdlowbenjamin</h3>
        </a>
    </contact>
</grid>

<script>
 import { stores } from '@sapper/app';
  const { page } = stores();
  $: title = generateTitle($page.path);
  $: console.log($page.path);
    
  function generateTitle(path) {
      if(path.startsWith("/blog")){
        return "BLOG";
      }else if(path.startsWith("/contact")){
        return "CONTACT";

      }else{
        return "BEN SWERDLOW"
      }
  }
</script>

<style>
    nav {
        position: absolute;
        top: 0;
        height: var(--nav-height);
        width: calc(100% - var(--side-nav-width));
        margin-left: var(--side-nav-width);
        border-bottom: 1px solid var(--accent);
    }
    nav h1 {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        padding-left: 15px;
        font-size: 28px;
        font-weight: 300;
        text-transform: uppercase;
        margin: 0px;
        color: var(--grey);
    }

    sidenav {
        height: 100%;
        width: var(--side-nav-width);
        position: fixed;
        display: flex;
        z-index: 1;
        top: 0;
        left: 0;
        writing-mode: tb-rl;
        border-right: 1px solid var(--accent);
    }

    .highlight {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 1px;
        z-index: 200;
        /* height: 25px; */
        background-color: white;
        margin-left: var(--side-nav-width);
        height: 80px;
        opacity: 1;
        transition: opacity 0.3s cubic-bezier(0.215, 0.61, 0.355, 1);
        animation: beam 6.5s cubic-bezier(0.77, 0, 0.175, 1) infinite;
    }

    @-webkit-keyframes beam {
        0% {
            transform: translateY(100vh);
        }
        20% {
            transform: translateY(-101%);
        }
        to {
            transform: translateY(-101%);
        }
    }

    @keyframes beam {
        0% {
            transform: translateY(100vh);
        }
        40% {
            transform: translateY(-101%);
        }
        to {
            transform: translateY(-101%);
        }
    }

    sidenav menu {
        padding: 0px;
        margin: 0px;
        width: var(--side-nav-width);
        align-items: center;
        overflow-x: hidden;
        writing-mode: tb-rl;
        justify-content: space-evenly;
        height: 100%;
        display: flex;
        border-bottom: 1px solid var(--accent);
    }

    socials {
        height: 120px;
        width: var(--side-nav-width);
        -webkit-transform: rotate(-90deg);
        -moz-transform: rotate(-90deg);
        -o-transform: rotate(-90deg);
        -ms-transform: rotate(-90deg);
        transform: rotate(-90deg);
        padding: 0px;
        margin: 0px;
    }

    socials table {
        width: 100%;
        height: 100%;
    }
    socials table tr {
        text-align: center;
    }

    socials table tr img {
        -webkit-transform: rotate(90deg);
        -moz-transform: rotate(90deg);
        -o-transform: rotate(90deg);
        -ms-transform: rotate(90deg);
        transform: rotate(90deg);
        width: 30px;
        fill: white;
    }

    a {
        text-decoration: none;
        text-transform: uppercase;
        color: var(--grey);
        font-size: 22px;
        -webkit-transform: rotate(180deg);
        -moz-transform: rotate(180deg);
        -o-transform: rotate(180deg);
        -ms-transform: rotate(180deg);
        transform: rotate(180deg);
    }
    main {
        margin-left: var(--side-nav-width);
        margin-top: var(--nav-height);
        padding-top: 1px;
        padding-left: 1px;
    }
</style>

<sidenav>
    <menu>
        <a href="blog">Blog</a>
        <a href="about">About</a>
        <a href="contact">Contact</a>
    </menu>
    <socials>
        <table>
            <tr>
                <td>
                    <a href="https://github.com/theswerd" target="_blank"><img
                            src="socials/github.svg"
                            alt="Github" /></a>
                </td>
                <td>
                    <a
                        href="https://instagram.com/ben_swerdlow"
                        target="_blank"><img
                            src="socials/instagram.svg"
                            alt="Instagram" /></a>
                </td>
            </tr>
            <tr>
                <td>
                    <a href="https://twitter.com/benswerd" target="_blank"><img
                            src="socials/twitter.svg"
                            alt="Twitter" /></a>
                </td>
                <td>
                    <a
                        href="https://www.linkedin.com/in/benswerdlow/"
                        target="_blank"><img
                            src="socials/linkedin.svg"
                            alt="LinkedIn" /></a>
                </td>
            </tr>
        </table>
    </socials>
</sidenav>
<div class="highlight" />
<nav>
    <h1>{title}</h1>
</nav>
<main>
    <slot />
</main>

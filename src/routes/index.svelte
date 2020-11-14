<script>
  import Technologies from "../components/homepage-parts/technologies.svelte";
  import Projects from "../components/homepage-parts/projects.svelte";
  import Testimonials from "../components/homepage-parts/testimonials.svelte";
  import Contact from "../components/homepage-parts/contact.svelte";

  import HomepageNav from "../components/homepage-parts/homepage-nav.svelte";
  let lastProgress = 0;
  let progress = 0;
  let body;
  let index = 0;

  function handleScroll(event) {
    //console.log(scrollAmount);
    lastProgress = progress;

    progress = event.target.scrollLeft / window.innerWidth;
  }

  //   $(window).on("scroll", function () {
  //     $("#realcontent").css("left", -$(window).scrollTop());
  //   });
</script>

<style>
  flexcontainer {
    display: flex;
    flex-flow: column;
    width: 100vw;
    height: 100vh;
  }
  .snap  {
    scroll-snap-type: x mandatory;
  }
  homepage {
    width: 100vw;
    height: 100%;
    flex: 1;
    display: flex;
    overflow-x: auto;
    transition: 300ms;
    transition-duration: 100ms;
    scroll-snap-type: none;
  }
  homepage::-webkit-scrollbar {
    display: none;
  }
</style>

<svelte:head>
  <title>Ben's Portfolio</title>
</svelte:head>
<flexcontainer>
  <HomepageNav bind:progress />
  <homepage on:scroll={handleScroll} bind:this={body} class="snap">
    <Technologies />
    <Projects />
    <Testimonials />
    <Contact />
  </homepage>
</flexcontainer>

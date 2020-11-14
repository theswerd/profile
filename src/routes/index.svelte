<script>
  import Technologies from "../components/homepage-parts/technologies.svelte";
  import Projects from "../components/homepage-parts/projects.svelte";
  import HomepageNav from "../components/homepage-parts/homepage-nav.svelte";

  let progress = 0;
  function handleScroll(event) {
	  
	progress =event.target.scrollLeft/window.innerWidth;
	console.log(progress);
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
  homepage {
    width: 100vw;
    height: 100%;
    flex: 1;
    display: flex;
    overflow-x: auto;
  }
  homepage::-webkit-scrollbar {
    display: none;
  }
</style>

<svelte:head>
  <title>Ben's Portfolio</title>
</svelte:head>
<flexcontainer>
  <HomepageNav bind:progress={progress}/>
  <homepage on:scroll={handleScroll}>
    <Technologies />
    <Projects />
  </homepage>
</flexcontainer>

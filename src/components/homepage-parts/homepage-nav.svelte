<script>
  export let progress;

  import Link from './nav/nav-link.svelte';
</script>

<style>
  navbar {
    position: fixed;
    height: 120px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  navbarBack {
    height: 120px;
    display: block;
  }
  navbar ul {
    justify-content: space-evenly;
    list-style: none;
    padding: 0;
    width: 100%;
    display: flex;
    justify-content:space-evenly;
    align-items: center;
  }


  .headshop {
    height: 80px;
    widows: 80px;
    border-radius: 40px;
  }
</style>

<navbar>
  <ul>
    <Link url="?tech" name="TECHNOLOGIES" selected={progress<1}/>
    <Link url="?projects" name="PROJECTS" selected={progress>=1 && progress <2}/>

    <img src="headshot.jpg" alt="Headshot" class="headshop" />
    <Link url="?testimonials" name="TESTIMONIALS" selected={progress>=2 && progress <3}/>
    <Link url="?contact" name="CONTACT" selected={progress>=3}/>
  </ul>
</navbar>
<navbarBack />

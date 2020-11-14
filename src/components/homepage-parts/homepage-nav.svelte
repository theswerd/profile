<script>
  export let progress;
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
  navbar ul li {
    align-items: center;
    padding: 0;
  }
  

  .headshop {
    height: 80px;
    widows: 80px;
    border-radius: 40px;
  }
</style>

<navbar>
  <ul>
    <li style={progress<1?"color:red":"color:blue"}>Technologies</li>
    <li style={progress>=1?"color:red":"color:blue"}>Projects</li>
    <img src="headshot.jpg" alt="Headshot" class="headshop" />
    <li>Testimonials</li>
    <li>Contact</li>
  </ul>
</navbar>
<navbarBack />

<script lang="ts">
  import _navbar from "../sass/components/_navbar.scss";
  import ChevronCircleUp from "svelte-icons/fa/FaBars.svelte";
  import Drawer from "./Drawer.svelte";

  let isDrawerOpen: boolean = false;

  const toggleNav = function () {
    isDrawerOpen = !isDrawerOpen;
    console.log(isDrawerOpen);
  };
</script>

<div>
  <div>
    <h1>Bernardo</h1>
  </div>
  <ul>
    <li>
      <a href="/About"> About</a>
    </li>
    <li><a href="/About"> Projects</a></li>
    <li><a href="/About"> Contact</a></li>
  </ul>
  <Drawer isOpen={isDrawerOpen} />
  <button on:click={toggleNav}> <ChevronCircleUp /> </button>
</div>

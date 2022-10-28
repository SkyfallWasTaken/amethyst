<script>
  import "virtual:windi.css";
  import "../app.css";

  import Sidebar from "../components/Sidebar.svelte";
</script>

<div class="flex h-screen select-none">
  <Sidebar />
  <main class="container p-5">
    <slot />
  </main>
</div>

<style>
  @font-face {
    font-family: "Fira Sans";
    src: url("/FiraSans-Medium.ttf") url("/FiraSans-Regular.ttf");
  }

  * {
    font-family: "Fira Sans";
  }
</style>

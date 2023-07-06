<script>
    import "../app.css";
	import Navbar from "../components/navbar.svelte";
  </script>
  

  <div class=" min-h-screen dark:bg-slate-800 dark:text-white bg-white relative">
    <div class="">
      <Navbar/>
    </div>
    <div class=" px-6 pt-14 lg:px-8">
  <slot />
</div>

</div>
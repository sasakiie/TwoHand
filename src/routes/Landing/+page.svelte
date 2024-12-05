<script>
  import NavBar from "../components/navigation.svelte";
  import Homepage from "./homepage.svelte";
  import MetaHead from "../components/MetaHead.svelte";
</script>

<div class="bg-gray-800">
  <MetaHead
    title="2hand E-commerce platform"
    description="A platform for buying and selling second-hand items."
  />
  <NavBar />
  <Homepage />
</div>

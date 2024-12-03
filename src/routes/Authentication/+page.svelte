<script>
    import Navbar from '../components/navigation.svelte'
    import UserRegister from './user-register.svelte';
    import MetaHead from  '../components/MetaHead.svelte';
    import NavBar from '../components/navigation.svelte';
</script>
<MetaHead
    title = "2hand E-commerce platform"
    description = "A platform for buying and selling second-hand items."
/>
<div>
    <NavBar/>
    <!-- <h1>Authentication</h1> -->
     <Navbar/>
    <UserRegister />
</div>
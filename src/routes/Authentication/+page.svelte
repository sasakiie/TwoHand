<script>
    import Navbar from '../components/navigation.svelte'
    import UserRegister from './user-register.svelte';
    import UserLogin from './user-login.svelte';
    import MetaHead from  '../components/MetaHead.svelte';
</script>

<MetaHead
    title = "2hand E-commerce platform"
    description = "A platform for buying and selling second-hand items."
    />

<div>
    <Navbar/>
    <UserRegister />
    <UserLogin />
</div>
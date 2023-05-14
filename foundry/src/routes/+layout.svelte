<script lang='ts'>
	// import '../theme.postcss';
	import { LightSwitch } from '@skeletonlabs/skeleton';
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import '../app.postcss';
	import Assets from '../components/assets.svelte';
	import Selector from '../components/selector.svelte';
	import Keys from '../components/keys.svelte';
	import Creds from '../components/creds.svelte';
	import Test from '../components/test.svelte';
  import Login from '../components/loginn.svelte';



  let isLoggedIn = getLoggedInStatus();

  function handleLoggedIn() {
    // Set the isLoggedIn variable to true when the user logs in
    isLoggedIn = true;
  }

  function getLoggedInStatus() {
  if (typeof document !== 'undefined') {
    const cookieValue = document.cookie
      .split('; ')
      .find(row => row.startsWith('loggedIn='))
      ?.split('=')[1];
    return cookieValue === 'true';
  } else {
    return false;
  }
}

function logOff() {
    document.cookie = "loggedIn=false; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
    window.location.reload();
  }


</script>
{#if !isLoggedIn}
  <Login on:loggedIn={handleLoggedIn} />
{/if}
<div class="lightswitch2">



  <button class="btn btn-sm   variant-filled " on:click={logOff}>Log off</button>


	<LightSwitch />
	<span class="chip variant-soft hover:variant-filled mt-2" >
		<span>GitHubs </span>
	</span>
</div>
{#if isLoggedIn}





<div class="container h-full  flex 	">

	<div class="left-sidebar">

	<Test />
	<Creds />
	</div>
	<div class="right-sidebar flex   w-full flex-col ">
    
	<Assets />
	<div class="flex flex-row">

		<Selector />
		<!-- <Keys /> -->
	</div>

	</div>

</div>
{/if}


<style>
	.lightswitch2{
		position: absolute;
		top: 2.5%;
		left: 95%;
	}
	.left-sidebar{
		/* background: white; */
		border-right: 2px solid rgb(187, 158, 29);
		width: 20%;
		height: 100vh;
	}
</style>


<!--  TODO  -->
<!-- CREATE A LIST OF JOBS THHAT WERE RUN A TABLE -->
<!-- MUST BE SHOWING -->
<!-- JOB NAME RUN-at thtat time status detailed information -->
<!-- BIlion row Demo  -  -->
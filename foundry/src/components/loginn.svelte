<script>
    import { createEventDispatcher } from 'svelte';
    import { ProgressRadial } from '@skeletonlabs/skeleton';
    let showForm = true;

    const dispatch = createEventDispatcher();
  
    function handleLogin() {
      document.cookie = "loggedIn=true";
  
      dispatch('loggedIn');
    }

    function simulateLoading() {
      showForm = !showForm;
    }

  </script>
  <div class="flex justify-center items-center p-0 w-[400px]  mt-[10%] mx-auto bg-white dark:bg-slate-800 rounded-lg 
   ring-1 ring-slate-900/5 shadow-xl " >

  <div class="login-form pt-10 pb-10  w-[100%] flex flex-col text-lg ">
    <svg class="mx-auto 	" xmlns="http://www.w3.org/2000/svg"  width="120" height="60"><path d="M153.7 54.5c-17.3 0-31.4 14-31.4 31.4a31.33 31.33 0 1 0 62.8 0c0-17.4-14.1-31.4-31.4-31.4zm0 47.1c-8.7 0-15.7-7-15.7-15.7s7-15.7 15.7-15.7 15.7 7 15.7 15.7-7 15.7-15.7 15.7zm55.1-5.2c0-2.5 3-3.7 4.7-1.9l20.9 21.8c.2.2.4.5 1.1.7.3.1.8.1 1.3.1H251c2.5 0 3.3-2.9 2.1-4.4l-23.5-24-1.2-1.3c-2.7-3.2-2.4-4.4.7-7.7L247.8 59c1.2-1.5.4-4.4-2.2-4.4h-12.8c-.5 0-.9 0-1.2.1-.8.2-1 .5-1.2.7-.1.1-10.4 11.2-16.7 18-1.7 1.9-4.8.6-4.8-1.9V35.9c0-1.8-1.5-2.5-2.7-2.5h-10.5c-1.8 0-2.7 1.2-2.7 2.3v79c0 1.8 1.5 2.3 2.7 2.3h10.5c1.6 0 2.7-1.2 2.7-2.4v-.8zm85.6 17.9l-1.1-10.5c-.2-1.4-1.5-2.4-2.9-2.2l-2.4.2c-8.4 0-15.2-6.6-15.6-14.8V73.3c0-1.7 1.2-3 2.9-3h14c1 0 2.5-.8 2.5-2.7v-9.9c0-1.9-1.2-3-2.3-3h-14.1c-1.6 0-3-1.2-3-2.8V36c0-1-.7-2.5-2.7-2.5h-10.4c-1.3 0-2.6.8-2.6 2.4V87c.4 16.9 14.3 30.5 31.4 30.5 1.4 0 2.8-.1 4.2-.3 1.2-.2 2.3-1.5 2.1-2.9zm75.6-13.2c-8.9 0-10.2-3.2-10.2-15.1V57.3c0-1-.7-2.7-2.7-2.7h-10.5c-1.3 0-2.7 1-2.7 2.7v1.3c-4.6-2.6-9.8-4.1-15.5-4.1-17.3 0-31.4 14-31.4 31.4a31.33 31.33 0 0 0 31.4 31.4c7.8 0 14.9-2.8 20.4-7.5 3 4.5 7.7 7.5 15.1 7.5 1.3 0 8 .2 8-2.9v-11.2c-.1-1-.9-2.1-1.9-2.1zm-41.6.5c-8.7 0-15.7-7-15.7-15.7s7-15.7 15.7-15.7 15.7 7 15.7 15.7c-.1 8.7-7.1 15.7-15.7 15.7z" transform="matrix(.400641 0 0 .400641 -38.998399 -.228366)" fill="#007dc1"/></svg>

    <svg class="mx-auto m-5" width="84px" height="84px" viewBox="0 0 32 32" enable-background="new 0 0 32 32" id="Layer_1" version="1.1" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g id="profile_x2C__person"> <g> <g> <g> <path d="M16,31C7.729,31,1,24.271,1,16S7.729,1,16,1s15,6.729,15,15S24.271,31,16,31z M16,2C8.28,2,2,8.28,2,16 s6.28,14,14,14s14-6.28,14-14S23.72,2,16,2z" fill="currentColor"></path> </g> </g> </g> <g> <g id="team_3_"> <g> <g> <g> <g> <path d="M23.64,20.713l-4.762-1.652l-0.323-2.584c-0.215,0.307-0.523,0.546-0.924,0.671l0.293,2.345 c0.023,0.189,0.152,0.349,0.332,0.41l5.055,1.756c0.9,0.314,1.689,1.427,1.689,2.381v-0.007c0,0.276,0.224,0.5,0.5,0.5 c0.275,0,0.499-0.223,0.5-0.498C25.997,22.656,24.94,21.168,23.64,20.713z" fill="currentColor"></path> </g> </g> </g> </g> <g> <g> <g> <g> <path d="M6.5,24.532c-0.276,0-0.5-0.224-0.5-0.5v0.007c0-1.379,1.059-2.871,2.359-3.326l4.762-1.641 l0.012-0.28c0.034-0.274,0.289-0.465,0.559-0.434c0.273,0.034,0.468,0.284,0.434,0.559l-0.051,0.589 c-0.023,0.189-0.153,0.348-0.333,0.41l-5.054,1.742C7.789,21.973,7,23.086,7,24.039v-0.007C7,24.309,6.776,24.532,6.5,24.532 z"
       fill="currentColor"></path> </g> </g> </g> </g> <g> <g> <g> <g> <g> <path d="M16,18.039c-2.779,0-4.192-1.844-4.201-6.469c-0.002-1.174,0.123-2.363,1.227-3.469 C13.729,7.396,14.729,7.039,16,7.039s2.271,0.357,2.975,1.063c1.104,1.105,1.229,2.295,1.227,3.469 C20.192,16.195,18.779,18.039,16,18.039z M16,8.039c-1.009,0-1.75,0.252-2.267,0.769c-0.632,0.633-0.938,1.2-0.935,2.761 c0.008,4.018,1.055,5.471,3.201,5.471s3.193-1.453,3.201-5.471c0.003-1.561-0.303-2.128-0.935-2.761 C17.75,8.291,17.009,8.039,16,8.039z" fill="currentColor"></path> </g> </g> </g> </g> </g> </g> </g> </g> </g></svg>
        <h3 class="mb-2 text-center ">Sign in</h3>
   

        <form on:submit|preventDefault={handleLogin}>
          {#if showForm}
            <label class="label mb-2 pl-10">
                <span >Username</span> 
                <input class="input w-[90%]  p-0.5 rounded-sm  " type="text" >
            </label> 

            <label class="label pl-10">
                <span>Password</span> 
                <input class="input w-[90%]  p-0.5 rounded-sm	"  type="password" >
              </label>
              
              
              
              <div class="text-center mt-6 pl-10 w-[90%]">
                <button type="submit" class="btn btn-sm text-lg variant-filled  w-[100%] rounded-sm	" >Sign in</button>
              </div>
              
              {/if}
            </form>
            {#if !showForm}
            <div class="mx-auto ml-[38%] mt-10 mb-16">
              <ProgressRadial ... stroke={20} meter="stroke-tertiary-500 dark:stroke-secondary-500" track="stroke-primary-500/30 dark:stroke-secondary-500/30"  width="w-24"   />
              </div>

            {/if}
          </div>
        </div>
        <button  on:click={simulateLoading}  class="btn btn-sm text-lg variant-filled   rounded-sm mt-4	" >Simulate Login Loading</button>
  


  
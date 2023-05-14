<div class="text-center w-100 ">
    <button on:click={toggleForm} 
    class="btn badge variant-filled pt-1 pb-1 m-0">Show Form</button>

</div>
{#if showForm}
<!-- <div class="modal_main bg-white dark:bg-slate-800 rounded-lg px-6 py-8 ring-1 ring-slate-900/5 shadow-xl " > -->
    <div class="fixed top-0 left-0 w-full h-full z-50 flex items-center justify-center bg-opacity-50 bg-gray-700">
        <div class=" min-w-[30%] bg-white dark:bg-slate-800 rounded-lg px-6 py-8 ring-1 ring-slate-900/5 shadow-xl " >
        <h3>Job 01 - AWX</h3>
    <form class="creds-form ">
        <label class="label ">
            <span>Key Name</span> 
            <input class="input" type="text" >
        </label> 
        
        <label class="label ">
            <span>Access Key</span> 
            <input class="input" type="password" >
        </label>
        
        <label class="label ">
            <span>Private Key</span> 
            <input class="input" type="password">
    </label>
    
    <div class="text-right mt-4">
        <button class="btn variant-filled btn-sm   ">Submit Form</button>
        <button on:click={closeForm} class="btn variant-filled btn-sm   ">Close Form</button>
    </div>

</form>
</div>
</div>

{/if}






<script>


  let showForm = false;
  function toggleForm() {
    showForm = true;
    document.body.classList.add("backdrop-blur-md");
  }

  function closeForm() {
    showForm = false;
    document.body.classList.remove("backdrop-blur-md");
  }


  function logOff() {
    document.cookie = "loggedIn=false; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
    window.location.reload();
  }
</script>

<style>

</style>
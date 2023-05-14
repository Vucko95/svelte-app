<!-- <div class=" card selector-container"> -->
        <div class="table-container">
            <!-- Native Table Element -->
            <table class="table table-hover">
                <thead>
                    <tr>
                        <th> CDP CREDENTAILS</th>
                        <th style="text-align: right;margin-right: 10px;">
                            <button  class="add_key badge variant-filled-primary mr-4" >
                                
                                <svg width="18px" height="18px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path fill-rule="evenodd" clip-rule="evenodd" d="M13.8067 6.07297C14.762 6.70986 14.9862 8.01853 14.2973 8.93707L13.2 10.4C12.9014 10.7981 12.941 11.3552 13.2929 11.7071L20.8073 19.2215L20.5621 19.7731C20.2421 20.4933 19.2535 20.5774 18.8163 19.9216L17.8321 18.4453C17.5257 17.9858 16.9049 17.8616 16.4453 18.168L15.9456 18.5011L14.9192 16.1061C14.8021 15.833 14.5698 15.6261 14.285 15.5415C14.0002 15.4568 13.6925 15.5032 13.4453 15.668L12.9456 16.0011L11.9192 13.6061C11.7983 13.3241 11.5547 13.1132 11.2583 13.0339C10.9619 12.9547 10.6455 13.0159 10.4 13.2L8.93707 14.2973C8.01853 14.9862 6.70986 14.762 6.07297 13.8067L3.19632 9.49169C2.66749 8.69844 2.77208 7.6422 3.4462 6.96807L6.96807 3.4462C7.6422 2.77208 8.69844 2.66749 9.49168 3.19632L13.8067 6.07297ZM16.0547 20.8321L16.7227 20.3868L17.1522 21.031C18.4637 22.9983 21.4295 22.7459 22.3898 20.5854L22.9138 19.4062C23.0819 19.0281 22.9997 18.5855 22.7071 18.2929L15.3204 10.9062L15.8973 10.1371C17.2751 8.29999 16.8267 5.68264 14.9161 4.40887L10.6011 1.53222C9.0146 0.474559 6.90212 0.683733 5.55386 2.03199L2.03199 5.55386C0.683733 6.90212 0.474558 9.0146 1.53222 10.6011L4.40887 14.9161C5.68265 16.8267 8.3 17.2751 10.1371 15.8973L10.5821 15.5635L11.5809 17.894C11.6979 18.167 11.9303 18.3739 12.2151 18.4586C12.4999 18.5432 12.8075 18.4969 13.0547 18.3321L13.5545 17.9989L14.5809 20.3939C14.6979 20.667 14.9303 20.8739 15.2151 20.9586C15.4999 21.0432 15.8075 20.9969 16.0547 20.8321ZM8.00003 10C9.1046 10 10 9.1046 10 8.00003C10 6.89546 9.1046 6.00003 8.00003 6.00003C6.89546 6.00003 6.00003 6.89546 6.00003 8.00003C6.00003 9.1046 6.89546 10 8.00003 10Z" 
                                    fill="currentColor"></path> </g></svg>
                                </button>
                            </th>
                        </tr>
                    </thead>

                <tbody>
                    <!-- {#each tableArr as row, i} -->
                        <tr>
                            <td>SandBox Key</td>
                           
                            <td> 
                                <SlideToggle name="slider-large" checked active="bg-primary-500" size="sm" />


                        </tr>
                        <tr>
                            <td>Demo Tenant Key</td>
                            <td> 
                                <SlideToggle name="slider-large"  active="bg-primary-500" size="sm" />
         
                                    <!-- <label class="relative inline-flex items-center  cursor-pointer">
                                        <input type="checkbox" value="" class="sr-only peer" >
                                        <div class="w-11 h-6 bg-gray-200 rounded-full peer
                                         dark:bg-gray-700 peer-focus:ring-4 peer-focus:ring-green-300 dark:peer-focus:ring-green-800
                                          peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute
                                           after:top-0.5 after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full 
                                           after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-green-600">
                                        </div>
                                      </label> -->
                            </td>         

                        </tr>
                        <tr>
                            <td>Personal Env </td>
                            <td> 
                                <SlideToggle name="slider-large"  active="bg-primary-500" size="sm" />

                            </td>
                        </tr>
                        <tr  >
                           
                            <td colspan="2" >
                                <!-- <button  class=" badge variant-filled-primary mr-4" >
                                    Add Key
                                    </button> -->
                                    
                            <div class="text-center w-100 ">
                                <button on:click={toggleForm} 
                                class="btn badge variant-filled pt-1 pb-1 m-0">Add  Key</button>

                            </div>
                            </td>
                            <!-- <td></td> -->
                            <!-- <td></td> -->
                        </tr>
    
    
                    <!-- {/each} -->
                </tbody>
                
            </table>
        </div>
        {#if showForm}
        <form class="creds-form">
            <label class="label text-center">
                <span>Key Name</span> 
                <input class="input" type="text" placeholder="Enter name...">
            </label> 

            <label class="label text-center">
                <span>Access Key</span> 
                <input class="input" type="password" placeholder="Enter Access Key">
            </label>

            <label class="label text-center">
                <span>Private Key</span> 
                <input class="input" type="password" placeholder="Enter Private key">
            </label>

             <div class="text-center mt-4">
                <button class="btn variant-filled ">Submit Form</button>
            </div>
        </form>
        {/if}
    
    
    
    <style>


    
    
        .table-container{
            width: 90%;
            margin-left: 2.5%;
            margin-top: 400px;
            /* height: 200px; */
        }
        .table-container thead, tbody tr,td,th {
            padding: 0.4rem;
            /* text-align: center; */
            vertical-align: middle;
            
        }
        .creds-form{
            padding: 20px;
            
        }
    

        
    
    </style>
    
    
    <script>
        import { SlideToggle } from '@skeletonlabs/skeleton';
        let showForm = false;
        function toggleForm() {
    showForm = !showForm;
  }


    </script>
<script>
  import { goto } from '$app/navigation';

  function gotoHome () {
    goto('/pages/home')
  }


    let showForm1 = true;
    let showForm2 = false;
  
    // @ts-ignore
    function toggleForm(form) {
      if (form === 1) {
        showForm1 = true;
        showForm2 = false;
      } else if (form === 2) {
        showForm1 = false;
        showForm2 = true;
      }
    }
</script>

<style>
  form {
    box-shadow: rgba(202, 202, 202, 0.633) 5px 5px 10px 1px;
    
  }
</style>

<!--MAIN BODY-->

  {#if showForm1}
  
    <form class="md:h-[80vh] md:w-[32vw] md:ml-10 lg:h-[70vh] h-[60vh] w-[80vw] bg-opacity-70  bg-[#fefefe] border-black  border-2 rounded-md ">
      <h1 class="md:text-[45px] text-[30px] mb-2 mt-5 text-slate-900 font-bold text-center md:mt-10 md:mb-8">LOGIN</h1>
      <div class="md:pl-9 md:pr-9 p-5">
        <label class="input input-bordered flex items-center gap-2 bg-slate-200 md:h-14 text-black border-slate-500 ">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="black" class="  w-4 h-4 opacity-70"><path d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6ZM12.735 14c.618 0 1.093-.561.872-1.139a6.002 6.002 0 0 0-11.215 0c-.22.578.254 1.139.872 1.139h9.47Z" /></svg>
          <input type="text" class="grow bg-slate-100 text-black " placeholder="Username" required />
        </label>
        <label class="input input-bordered flex items-center gap-2 bg-slate-200 mt-7 md:h-14 text-black border-slate-500 ">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="black" class="w-4 h-4 opacity-70"><path fill-rule="evenodd" d="M14 6a4 4 0 0 1-4.899 3.899l-1.955 1.955a.5.5 0 0 1-.353.146H5v1.5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-2.293a.5.5 0 0 1 .146-.353l3.955-3.955A4 4 0 1 1 14 6Zm-4-2a.75.75 0 0 0 0 1.5.5.5 0 0 1 .5.5.75.75 0 0 0 1.5 0 2 2 0 0 0-2-2Z" clip-rule="evenodd" /></svg>
          <input type="password" class="grow " value="" placeholder="Password" required />
        </label>
        <p class="text-slate-800 float-end mt-4 font-medium text-[12px] md:text-[15px]">Forgot password?</p>
        
        <button on:click={gotoHome}  class="btn  mt-5 w-[100%] text-[18px]">ENTER</button>
      </div>
    
      <div class="text-center ">
        <p class=" text-black font-medium text-center text-[15px]">Don't have account? <button on:click={() => toggleForm(2)} class=" text-black hover:text-blue-900 hover:font-bold font-bold rounded-md hover:text-[#005CED] ">Register</button> </p>
      </div>
      
    </form>







  {:else if showForm2}
  <form class="md:h-[80vh] h-[73vh] mt-[-30px] md:mt-[-20px] md:w-[32vw] md:ml-10 lg:h-[75vh]  w-[80vw] bg-opacity-70  bg-[#fefefe] border-black  border-2 rounded-md ">
    <h1 class="md:text-[45px] text-[30px] mb-1 mt-2 text-slate-900 font-bold text-center  lg:m-5  ">REGISTER</h1>
    <div class="md:pl-9 md:pr-9 p-3">
      <label class="input input-bordered flex items-center gap-2 bg-slate-200 md:h-14 text-black border-slate-500 ">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="black" class="  w-4 h-4 opacity-70"><path d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6ZM12.735 14c.618 0 1.093-.561.872-1.139a6.002 6.002 0 0 0-11.215 0c-.22.578.254 1.139.872 1.139h9.47Z" /></svg>
        <input type="text" class="grow bg-slate-100 text-black " placeholder="Username" required />
      </label>
      <label class="input input-bordered flex items-center gap-2 bg-slate-200 mt-4 md:h-14 text-black border-slate-500 ">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4 opacity-70"><path d="M2.5 3A1.5 1.5 0 0 0 1 4.5v.793c.026.009.051.02.076.032L7.674 8.51c.206.1.446.1.652 0l6.598-3.185A.755.755 0 0 1 15 5.293V4.5A1.5 1.5 0 0 0 13.5 3h-11Z" /><path d="M15 6.954 8.978 9.86a2.25 2.25 0 0 1-1.956 0L1 6.954V11.5A1.5 1.5 0 0 0 2.5 13h11a1.5 1.5 0 0 0 1.5-1.5V6.954Z" /></svg>
        <input type="email" class="grow bg-slate-100 text-black " placeholder="Email" required />
      </label>
      <label class="input input-bordered flex items-center gap-2 bg-slate-200 mt-4 md:h-14 text-black border-slate-500 ">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="black" class="w-4 h-4 opacity-70"><path fill-rule="evenodd" d="M14 6a4 4 0 0 1-4.899 3.899l-1.955 1.955a.5.5 0 0 1-.353.146H5v1.5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-2.293a.5.5 0 0 1 .146-.353l3.955-3.955A4 4 0 1 1 14 6Zm-4-2a.75.75 0 0 0 0 1.5.5.5 0 0 1 .5.5.75.75 0 0 0 1.5 0 2 2 0 0 0-2-2Z" clip-rule="evenodd" /></svg>
        <input type="password" class="grow " value="" placeholder="Password" required />
      </label>
      <label class="input input-bordered flex items-center gap-2 bg-slate-200 mt-4 md:h-14 text-black border-slate-500 ">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="black" class="w-4 h-4 opacity-70"><path fill-rule="evenodd" d="M14 6a4 4 0 0 1-4.899 3.899l-1.955 1.955a.5.5 0 0 1-.353.146H5v1.5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-2.293a.5.5 0 0 1 .146-.353l3.955-3.955A4 4 0 1 1 14 6Zm-4-2a.75.75 0 0 0 0 1.5.5.5 0 0 1 .5.5.75.75 0 0 0 1.5 0 2 2 0 0 0-2-2Z" clip-rule="evenodd" /></svg>
        <input type="password" class="grow " value="" placeholder="Confirm Password" required />
      </label>  
      <p class="text-slate-800 float-end mt-2 font-medium text-[12px] md:text-[15px]">Forgot password?</p>
      
      <button class="btn  mt-2 w-[100%] text-[18px]">SUBMIT</button>
    </div>
  
    <div class="text-center ">
      <p class=" text-black font-medium text-center text-[15px]">Have an account? <button on:click={() => toggleForm(1)} class=" text-black hover:text-blue-900 hover:font-bold font-bold rounded-md hover:text-[#005CED] ">Login</button> </p>
    </div>
    
  </form>




    
  {/if}

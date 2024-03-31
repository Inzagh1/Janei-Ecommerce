<script>
  import Footerhome from "../../../components/footerhome.svelte";
  import Chatbubble from "../../../components/chatbubble.svelte";
  import Header from "../../../components/header.svelte";


</script>
<style>
    .text {
        filter: drop-shadow(0 0 10px  rgba(7, 7, 7, 0.552));
    }
    .lanyard {
      filter: drop-shadow(0 0 10px  rgb(255, 255, 255));
    }
    .ellipse {
      border-radius: 50%/50%; 
      filter: drop-shadow(0px 15px 5px  rgba(3, 3, 3, 0.552));
  }
</style>
<main class="relative bg-[#d9d9d9]">
  <Header/>
  <section class="z-10">
    <!-- HOME PAGE -->
    <div class="h-screen w-full">
      <div class="flex flex-col p-5 md:flex-row md:p-10 ">
        <div class="flex-grow bg-gray-200 h-56   md:h-auto md:w-1/2 md:flex md:items-center">
          <div class="md:h-auto md:mt-[-15%] justify-center text-center md:text-left md:pl-10 ">
              <span class="text text-black text-[22px]  font-semibold md:text-[32px]">
                LANYARD DESIGN <br/>
              </span>
              <span class="text text-black text-[40px] font-bold md:text-[55px]">
                FOR BUILDERS <br/>  
              </span>
              <span class="text text-black text-[15px] font-bold md:text-[22px]">
                Janei Editing and Printing Services
              </span> <br/>
              <div class="w-[50%] h-[3px] md:float-start mx-auto mt-2 md:h-1.5 bg-black md:mt-5"></div>
              <div class="md:pt-10 pt-3">
                <button class="flex items-center mx-auto md:float-start   text-black text-[12px] font-semibold p-1 rounded-md
                  md:text-[17px] md:font-bold  md:p-3 md:pr-5 md:pl-5 bg-slate-100 hover:bg-yellow-600 duration-200 hover:scale-[97%] 
                    shadow-md shadow-[#0000007f]  border-black border
                    md:rounded-tl-[20px]  md:rounded-tr-[40px]  md:rounded-bl-[40px]  md:rounded-br-[20px]    ">
                  <h1 class="md:block "> ORDER NOW </h1>
                  <box-icon type='solid' name='cart-alt' class="ml-2"></box-icon>
                </button>
              </div>
          </div>
        </div>
        
        <div class="flex-grow bg-gray-300 h-[100%]  md:h-auto md:w-1/3 md:flex md:justify-center md:items-center">
         
            <img src="/homeimg.png" alt="logo" srcset="" class="lanyard z-20  mx-auto justify-center items-center h-[350px] mt-[-7%]  md:h-[105%] shadow-text-white drop-shadow-lg md:mt-[-55%]">
            <div class="ellipse hidden md:block bg-[#FBFBFB] h-[60px]  w-[100%] md:mt-[135%] ml-[-100%]
           
            "></div>

        </div>
        
        <div class="flex-grow bg-gray-400 h-44 md:h-auto md:w-1/2 md:flex md:justify-center md:items-center">
        d
        </div>
      </div>
    </div>
    <!-- ABOUT US PAGE -->
    <div class="h-screen"></div>
    <!-- FAQ PAGE -->
    <div class="h-screen"></div>
  </section>
  <div class="z-50 fixed bottom-4 right-3 md:right-10">
    <Chatbubble/>
  </div>
</main>

<Footerhome/> 

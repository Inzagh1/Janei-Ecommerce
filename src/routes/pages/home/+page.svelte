<script>
  import Footerhome from "../../../components/footerhome.svelte";
  import Chatbubble from "../../../components/chatbubble.svelte";
  import Header from "../../../components/header.svelte";


</script>

<main class="relative bg-[#d9d9d9]">
  <Header/>
  <section class="z-10">
    <div class="h-screen w-full">
      <div class="h-[550px] w-[650px] mt-16 border-black border mx-auto bg-cover bg-center shadow-md shadow-black" style="background-image: url('/images.jpg');"></div>
    </div>
    <div class="h-screen"></div>
    <div class="h-screen"></div>
  </section>
  <div class="z-50 fixed bottom-4 right-4">
    <Chatbubble/>
  </div>
</main>

<Footerhome/> 

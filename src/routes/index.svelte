<script>
  import LG from '../lib/Components/Login.svelte'
  import CL from '../lib/Components/ConformLog.svelte'
  import SN from '../lib/Components/SNP.svelte'
  import LO from '../lib/Components/Logout.svelte'
    // console.log("Hello world")
</script>

<svelte:head>
    <title>Home</title>
</svelte:head>

<!-- <div>
  <SN/>
  <div>
    <CL/>
    <div>
      <LG/>
    </div>
  </div>
</div>

<br><br><br><br>
<LO/> -->
 <style>
  .bg{
      background: radial-gradient(50% 50% at 50% 50%, #FFFFFF 0%, #868282 100%);
  }
  .r{
      background: linear-gradient(180deg, #423FD2 0%, #C73FD2 100%);
  }
  .z{
      position: relative;
     left: 0px;
     top: 0px;
    z-index: 1;
  }
  .t{
      color: #AB3FD2;
  }
  .bt{
    background: linear-gradient(270deg, #4E3FD2 -7.17%, #A53FD2 107.97%);
    border-radius: 15px;
  }
</style>
<div>
  <body class="bg">
   <div class="">
    <header class="text-gray-600 body-font">
      <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
        <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
          
          <span class="ml-3 text-5xl">ReachMe</span>
        </a>
        <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center text-2xl">
          <a class="mr-5 text-gray-900 hover:text-blue-900">Home</a>
          <a href="/About" class="mr-5 text-gray-900 hover:text-blue-900">About</a>
          <a href="/Help" class="mr-5 text-gray-900 hover:text-blue-900">Help</a>
          <a href="/Contact" class="mr-5 text-gray-900 hover:text-blue-900">Contact Us</a>
          <a href="/SNP">
            <button class="bt rounded-full text-white px-4 border-2 focus:outline-none">Sign In</button>
          </a>
        </nav>
      </div>
    </header>
   </div>
      <div class="grid grid-cols-2 mt-44">
          <div class="z ml-72 -mt-28">
              <div class="-ml-8">
              <img class="w-44 ml-96" src="img/lady.png" alt="">
              </div>
          </div>
          <div class="-mt-20 -ml-2">
              <div class="r -mt-20 -ml-8  rounded-full h-44 w-44"></div>
          </div>
      </div>
      <div class="grid grid-cols-2 absolute top-1/2 text-center ml-72">
          <div class="z text-5xl font-semibold mt-4 ml-28">Live for your</div>
          <div class="t text-6xl font-semibold mt-24 ml-26"><span class="z">PASSION</span></div>
          </div>
  </body>
</div>



       
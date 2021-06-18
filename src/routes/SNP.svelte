  <script>
    let formobj = {
     "user":"",
   "pass":""
    }
    let apidata= {
   "auth":"signup",
   "c_id":"3v9h9sli9f0c4bhepe81vsho1j",
   "user":"",
   "pass":"",
   
    }
    async function handlesubmit() {
   apidata.user=formobj.user
   apidata.pass=formobj.pass
     const res = await fetch("https://nvq772gy0f.execute-api.ap-south-1.amazonaws.com/default/botocognitoauth",{
      method:'POST',
      mode:"cors",
   headers:{
   "X-API-KEY":"xnFSKlZEm01aSvcgdd7Bx5ttpzyF494F1WOF0JvZ",
      "Content-Type":"application/json"
   },
   body:JSON.stringify(apidata)
   
   });
   console.log(res.status)
   res.json().then((e) =>{
   console.log(e)
     alert(e.error)
   });
    }
   
   </script>
   


   <style>
    .bg{
     position: absolute;
width: 290px;
height: 450px;
left: 585px;
top: 423px;

background: linear-gradient(312.42deg, rgba(255, 19, 72, 0.5355) 24.09%, rgba(174, 64, 211, 0.408) 50%), linear-gradient(180deg, #6F4CD5 0%, #EB1447 88.46%);
border: 1px solid rgba(0, 0, 0, 0.75);
    }
   .bg1{
    
width: 1350px;
height: 640px;

background: linear-gradient(180deg, #654DD5 0%, #B23FD2 100%), #593FD2;
   }
   .ig{
    position: absolute;
width: 900px;
height: 500px;
left: 75px;
top: 157px;

   }
   
   
</style>

<div class="bg1">
  <div class="ig -mt-32 ml-20">
    <img class="" src="img/r71.png" alt="">
  </div>
<div class="bg -mt-80 ml-4 rounded-lg">
<div class="text-white text-center mt-8 font-bold">
    SIGN IN
</div>
<div class="ml-20 mt-2">
  <img class="rounded-full h-24 w-24 ml-2" src="img/r8.png" alt="">
</div>
<div class="relative">
    <label for="name" class="leading-7 text-sm text-gray-600">Email-Id</label>
    <input class="rounded-full ml-2" type="text"  bind:value={formobj.user}>
   </div>
<div class="relative">
    <label for="name" class="leading-7 text-sm text-gray-600">Password</label>
  <input class="rounded-full ml-2" type="password"  placeholder="Password" bind:value={formobj.pass}>
</div>
<div class="p-2 w-full">
   <button class="flex mx-auto text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg" on:click={handlesubmit}>
   Submit
   </button>
  </div>
    
   
    {JSON.stringify(formobj)}
   {JSON.stringify(apidata)}
</div>
</div>
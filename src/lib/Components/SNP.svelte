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
   
    
   <div class="relative">
    <label for="name" class="leading-7 text-sm text-gray-600">Email-Id</label>
    <input type="text"  bind:value={formobj.user}>
   </div>
     <div class="relative">
      <label for="name" class="leading-7 text-sm text-gray-600">Password</label>
    <input type="password"  bind:value={formobj.pass}>
   </div>
   <div class="p-2 w-full">
   <button class="flex mx-auto text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg" on:click={handlesubmit}>
   Submit
   </button>
  </div>
    
   
    {JSON.stringify(formobj)}
   {JSON.stringify(apidata)}


   <style>
    .bg{
     position: absolute;
width: 251px;
height: 391px;
left: 585px;
top: 423px;

background: linear-gradient(312.42deg, rgba(255, 19, 72, 0.5355) 24.09%, rgba(174, 64, 211, 0.408) 50%), linear-gradient(180deg, #6F4CD5 0%, #EB1447 88.46%);
border: 1px solid rgba(0, 0, 0, 0.75);
    }
   
</style>

<div class="bg -mt-72">
<div class="">
    SIGN IN
</div>
</div>
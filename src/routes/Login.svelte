<script>
    let formobj = {
     "user":"",
   "Pass":""
    }
    let apidata= {
 "auth": "login",
"pool_id":"ap-south-1_9WoXGfjYO",
"c_id": "3v9h9sli9f0c4bhepe81vsho1j",
"user": "",
"pass": ""

                                                       
    }
    async function handlesubmit() {
   apidata.user=formobj.user
   apidata.pass=formobj.Pass
     const res = await fetch("https://nvq772gy0f.execute-api.ap-south-1.amazonaws.com/default/botocognitoauth",{
      method:'POST',
      mode:"cors",
      // credentials:'include',
   headers:{
   "X-API-KEY":"xnFSKlZEm01aSvcgdd7Bx5ttpzyF494F1WOF0JvZ",
      "Content-Type":"application/json"
   },
   body:JSON.stringify(apidata)
   
   });
   console.log(res.status)
   res.json().then((e) =>{
     console.log(e)
   })
    }
   
   </script>
   <div>
   User : <input type="text" bind:value={formobj.user}>
   </div>
     <div>
   Password : <input type="password" bind:value={formobj.Pass}>
   </div>
   <button on:click={handlesubmit}>
   Submit
   </button>
    
   
   {JSON.stringify(formobj)}
   {JSON.stringify(apidata)} 

   
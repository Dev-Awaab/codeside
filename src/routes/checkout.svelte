<script>
    import axios from 'axios'
    import { useLoc } from '../store/loc'
    import { onMount } from 'svelte'
    import { getCheckout } from '../store/cartStore'

    onMount( async () => {

        //  let getCheckout;

        await useLoc
        
        // haeders 
        const config = {
            headers: {
                'user-token': `${$useLoc.detail.access_token}`
            }
        }

        // checkout req
        const { data } = await axios.get('https://aqueous-beyond-13704.herokuapp.com/checkout', config)

        $getCheckout = data
    })
   
    const cart = $useLoc.detail.cart
    
</script>

<main class='h-screen md:mx-40'>
       {#if cart.length === 0}
            <div class='text-center my-10 '>
                 <h1 class='font-bold my-5 text-lgblue'>Ooops your cart is empty!</h1>
                  <a href="/" class='bg-drblue px-3 py-3 rounded text-white hover:bg-lgblue'>Keep Shopping</a>
            </div>
          {:else}
           {#if $getCheckout.status_code === 200}
              <h3 class='text-center'>
                  {$getCheckout.detail}
              </h3>
           {/if}
           
       {/if}

    <!-- <div class=" p-5 bg-gray-800 rounded overflow-visible md:m-12 m-10">
         <span class="text-xl font-medium text-gray-100 block pb-3">Card Details</span>
          <span class="text-xs text-gray-400 ">Card Type</span>
        <div class="overflow-visible flex justify-between items-center mt-2">
            <div class="rounded w-52 h-28 bg-gray-500 py-2 px-4 relative right-10"> <span class="italic text-lg font-medium text-gray-200 underline">VISA</span>
                <div class="flex justify-between items-center pt-4 "> <span class="text-xs text-gray-200 font-medium">****</span> <span class="text-xs text-gray-200 font-medium">****</span> <span class="text-xs text-gray-200 font-medium">****</span> <span class="text-xs text-gray-200 font-medium">****</span> </div>
                <div class="flex justify-between items-center mt-3"> <span class="text-xs text-gray-200">John Doe</span> <span class="text-xs text-gray-200">12/18</span> </div>
            </div>
            <div class="flex justify-center items-center flex-col"> <img src="https://img.icons8.com/color/96/000000/mastercard-logo.png" width="40" class="relative right-5" /> <span class="text-xs font-medium text-gray-200 bottom-2 relative right-5">mastercard.</span> </div>
        </div>
        <div class="flex justify-center flex-col pt-3"> <label class="text-xs text-gray-400 ">Name on Card</label> <input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="John Doe"> </div>
        <div class="flex justify-center flex-col pt-3"> 
            <label class="text-xs text-gray-400 ">Card Number</label>
             <input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="**** **** **** ****"> </div>
        <div class="grid grid-cols-3 gap-2 pt-2 mb-3">
            <div class="col-span-2 "> <label class="text-xs text-gray-400">Expiration Date</label>
                <div class="grid grid-cols-2 gap-2"> <input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="mm"> <input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="yyyy"> </div>
            </div>
            <div class=""> <label class="text-xs text-gray-400">CVV</label> <input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="XXX"> </div>
        </div> <button class="h-12 w-full bg-blue-500 rounded focus:outline-none text-white hover:bg-blue-600">Check Out</button>
    </div> -->
</main>
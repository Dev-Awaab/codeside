
<script>
    //  import Hamburger from '../Hamburger.svelte'

    //  export let sidebar = false
</script>


<header class='flex justify-between p-3 border-b-2 border-gray-200 sticky'>
    <div class='flex'>
    <a href='/#'>
        
        <img src="/code_logo.png" alt="" class='h-10 hidden md:block'>
    </a>
        <h1 class='ml-3 py-2 text-bold text-drblue'>CodeSide</h1>
      
    </div>


    <ul class='flex m-2' >
        <li class='px-2'>
            <a href='/tt'>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chat icon" viewBox="0 0 16 16">
                    <path d="M2.678 11.894a1 1 0 0 1 .287.801 10.97 10.97 0 0 1-.398 2c1.395-.323 2.247-.697 2.634-.893a1 1 0 0 1 .71-.074A8.06 8.06 0 0 0 8 14c3.996 0 7-2.807 7-6 0-3.192-3.004-6-7-6S1 4.808 1 8c0 1.468.617 2.83 1.678 3.894zm-.493 3.905a21.682 21.682 0 0 1-.713.129c-.2.032-.352-.176-.273-.362a9.68 9.68 0 0 0 .244-.637l.003-.01c.248-.72.45-1.548.524-2.319C.743 11.37 0 9.76 0 8c0-3.866 3.582-7 8-7s8 3.134 8 7-3.582 7-8 7a9.06 9.06 0 0 1-2.347-.306c-.52.263-1.639.742-3.468 1.105z"/>
                  </svg>
            </a>
        </li>
        <li class='px-2'>
            <a href='/tt'>
                <svg  xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-bell icon" viewBox="0 0 16 16">
                    <path d="M8 16a2 2 0 0 0 2-2H6a2 2 0 0 0 2 2zM8 1.918l-.797.161A4.002 4.002 0 0 0 4 6c0 .628-.134 2.197-.459 3.742-.16.767-.376 1.566-.663 2.258h10.244c-.287-.692-.502-1.49-.663-2.258C12.134 8.197 12 6.628 12 6a4.002 4.002 0 0 0-3.203-3.92L8 1.917zM14.22 12c.223.447.481.801.78 1H1c.299-.199.557-.553.78-1C2.68 10.2 3 6.88 3 6c0-2.42 1.72-4.44 4.005-4.901a1 1 0 1 1 1.99 0A5.002 5.002 0 0 1 13 6c0 .88.32 4.2 1.22 6z"/>
                  </svg>
            </a>

        </li> 
        <li class='px-2'>
            <a href='/tt'>
              <img src="/inst.jpeg" class="w-10 rounded-full" alt="">
            </a>
        </li>
        <li class='px-2'>
            <a href='/cart'>
                <i class='bx bxs-cart-add icon'></i> 
            </a>
        </li>
    </ul>
</header>


<style>
    .icon{
     font-size: 30px;
     color: #6363A3;
    }
</style>
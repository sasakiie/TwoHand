<div class="min-h-screen py-48 bg-gradient-to-r from-sky-500 to-indigo-500 ">
    <div class="container mx-auto ">
        <div class="flex flex-col lg:flex-row w-10/12 lg:w-8/12 bg-white rounded-xl mx-auto shadow-lg overflow-hidden  ">
            <div class="w-full lg:w-1/2 flex flex-col items-center justify-center p-12 bg-no-repeat bg-cover bg-center bg-[#058CD7]">
                <img src="/logo.png" alt="" class=" w-[274px] ">                
            </div>
            <div class="w-full lg:w-1/2 py-16 px-12">
                <h2 class="text-3xl mb-4">Register</h2>
                <p class="mb-4">
                    &nbsp;&nbsp;&nbsp;Create your account.
                </p>
                <form action="#">
                    <div class="grid grid-cols-2 gap-5">
                        <input type="text" placeholder="FirstName" class="shadow border rounded-full py-1 px-2 text-gray-700 leading-tight focus:outline-none">
                        <input type="text" placeholder="SurName" class="shadow border rounded-full py-1 px-2 text-gray-700 leading-tight focus:outline-none">
                    </div>
                    <div class="mt-5">
                        <input type="email" placeholder="Email" class=" w-full shadow border rounded-full py-1 px-2 text-gray-700 leading-tight focus:outline-none">
                    </div>
                    <div class="mt-5">
                        <input type="password" placeholder="Password" class=" w-full shadow border rounded-full py-1 px-2 text-gray-700 leading-tight focus:outline-none">
                    </div>
                    <div class="mt-5">
                        <input type="password" placeholder="Confirm Password" class=" w-full shadow border rounded-full py-1 px-2 text-gray-700 leading-tight focus:outline-none">
                    </div>
                    <div class="mt-5">
                        <button 
                        type="submit"
                        class="bg-red-500 hover:bg-red-700 
                        text-white font-bold py-2 px-4 rounded-full focus:outline-none w-full">
                        REGISTER
                    </button>
                    </div>
                    <div class="mt-5 text-center">
                        <p class="text-gray-600 text-sm">
                          Already have an account? 
                          <a href="/login" class="text-blue-500 hover:underline">Log in</a>
                        </p>
                      </div>
                    </form>
            </div>
        </div>
    </div>
</div>
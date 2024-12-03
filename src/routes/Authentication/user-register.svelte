

<div class="flex flex-col justify-center items-center h-screen bg-gradient-to-r from-sky-500 to-indigo-500">
    <h1 class="text-3xl font-bold text-white">Welcome to</h1> <br>
    <img src="/logo.png" alt="" class=" w-[274px] ">
    <form class="bg-[#058CD7] px-8 pt-6 pb-8 mb-4">
        <div class="mb-4">
            <label for="First_Name" class="block text-white text-sm font-bold mb-2">
                First Name
            </label>
            <input class="shadow border rounded-full w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none" 
            type="text" 
            name="First_Name"
            id="First_Name" />
        </div>
        <div class="mb-4">
            <label for="Last_Name" class="block text-gray-700 text-sm font-bold mb-2">
                Last Name
            </label>
            <input class="shadow border rounded-full w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none" 
            type="text" 
            name="Last_Name"
            id="Last_Name" />
        </div>
        <div class="mb-4">
            <label for="email" class="block text-gray-700 text-sm font-bold mb-2">
                Email
            </label>
            <input class="shadow border rounded-full w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none" 
            type="email" 
            name="email"
            id="email" />
        </div>
        <div class="mb-4">
            <label for="password" class="block text-gray-700 text-sm font-bold mb-2">
                Password
            </label>
            <input class="shadow border rounded-full w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none" 
            type="password" 
            name="password"
            id="password" />
        </div>
        <div class="mb-4">
            <label for="password_confirm" class="block text-gray-700 text-sm font-bold mb-2">
                Confirm Password
            </label>
            <input class="shadow border rounded-full w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none" 
            type="password" 
            name="password_confirm"
            id="password_confirm" />
        </div> <br>
        <div class="flex items-center">
            <button 
                type="submit"
                class="bg-red-500 hover:bg-red-700 
                text-white font-bold py-2 px-4 rounded-full focus:outline-none w-full">
                REGISTER
            </button>
        </div>
    </form>
</div>
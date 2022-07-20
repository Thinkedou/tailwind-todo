<template>
      <div class="container w-full max-w-2xl " id='app'>
        <div class="text-3xl text-center font-bold mb-3 uppercase ">Todo List in tailwind</div>
        <div >
            <div class="flex justify-center">
                <input type="text" name="todo"  placeholder="Enter Todo" class="text-xl text-indigo-800 placeholder-indigo-400 py-2 px-5 bg-indigo-100 rounded-l-full outline-indigo-300">
                <button type="submit" class="text-xl text-indigo-100 placeholder-indigo-400 py-2 pr-5 pl-4 bg-indigo-500 rounded-r-full">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
                    </svg>
                </button>
            </div>
        </div>
        <div class="bg-gray-100 mt-5 p-5 rounded-xl shadow-lg text-gray-700">
            <h1 class="font-bold text-xl italic block mb-0 leading-none">Todo's</h1>
            <small id="todo_stats" class="block mb-5 mt-0 text-xs text-gray-500">3 Todos pending, 2 Completed.</small>
            <div class="max-h-80 overflow-y-auto">
                <table id="todo_table" class="table w-full">
                    <thead>
                        <tr>
                            <th class="text-center px-1 py-2 bg-indigo-500 text-indigo-100 rounded-tl-xl">#</th>
                            <th class="text-left px-1 py-2 bg-indigo-500 text-indigo-100">Details</th>
                            <th class=" px-1 py-2 bg-indigo-500 text-indigo-100 rounded-tr-xl">Action</th>
                        </tr>
                    </thead>
                    <tbody >
                        <tr class="odd:bg-indigo-100 even:bg-indigo-50">
                            <td class="text-center  px-1 py-2 text-indigo-800" colspan="3">Rien à faire? ajouter une tâche</td>
                        </tr>
                        <tr class="odd:bg-indigo-100 even:bg-indigo-50 transition duration-300">
                            <td class="text-center  px-1 py-2 text-indigo-800">2</td>
                            <td class=" px-1 py-2 text-indigo-800">Un truc à faire</td>
                            <td class="text-center  px-1 py-2 text-indigo-800 flex gap-3 justify-start">
                               <button class="text-indigo-600">   <!-- tâche completé  -->
                                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                                    </svg>
                                </button>
                                <button class="text-indigo-600"> <!-- remettre incomplète  -->
                                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                                    </svg>
                                </button>
                                <button  class="text-indigo-600"> <!-- supprimer la tâche -->
                                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                        <path stroke-linecap="round" stroke-linejoin="round" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
                                    </svg>
                                </button>
                            </td>
                        </tr>
                        
                        
                    </tbody>
                </table>
            </div>  
        </div>
    </div>

</template>
<script>
export default {
  name:'App',
  created(){
    let classArray = ['bg-yellow-50','flex','justify-center','items-center','h-screen']
     document.body.classList.add(...classArray);
  }
}
</script>
<style>

</style>

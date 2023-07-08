<script>
export default {

}
</script>
<template>
     <main>
          <hr>
          <nav class="questionnaire-info-plus-person-info flex justify-evenly">
               <nav>

                    <button class="mt-3 link rounded-t-lg border-2 border-gray-300 ms-2"
                         style="border-bottom: none;">アンケート情報</button>

                    <nav class="border-2 border-gray-300 rounded-lg p-6 w-96">

                         <div style="display: flex; justify-content: flex-end;">
                              <input class="border-b border-black focus:border-primary focus:outline-none w-24">
                              <p>~</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-24">
                         </div>


                         <div class="text-center mt-3">
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full">
                         </div>
                         <div class="text-center mt-3">
                              <textarea name="description" v-model="description"
                                   style="border: 1px solid gray; border-radius: 5px; padding: 8px;" rows="4" cols="30"
                                   placeholder="説明内容"></textarea>
                         </div>
                    </nav>
               </nav>

               <nav class="person-info mt-3">
                    <button class="link rounded-t-lg border-2 border-gray-300 ms-2"
                         style="border-bottom: none;">個人情報</button>
                    <nav class="search-area border-2 border-gray-300 rounded-lg p-6 w-96">
                         <div class="title-area mb-2">
                              <p>名前</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="プロジェクト名を入力でください">
                         </div>
                         <div class="title-area mb-2">
                              <p>メール</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="メールを入力でください">
                         </div>
                         <div class="title-area mb-2">
                              <p>年齢</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="年齢を入力でください">
                         </div>
                         <div class="title-area mb-2">
                              <p>性別</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="性別を入力でください">
                         </div>
                         <div class="title-area mb-2">
                              <p>住所</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="住所を入力でください">
                         </div>
                         <div class="title-area mb-2">
                              <p>電話番号</p>
                              <input class="border-b border-black focus:border-primary focus:outline-none w-full md:w-72"
                                   placeholder="電話番号を入力でください">
                         </div>
                    </nav>
               </nav>

          </nav>
          <hr class="mt-3">

          <nav class="questions mt-3 mb-3 flex justify-center">

               <nav>
                    <button class="link rounded-t-lg border-2 border-gray-300 ms-2" style="border-bottom: none;">問題</button>
                    <nav class="border-2 border-gray-300 rounded-lg p-6" style="width: 700px;">
                         <p class="question">-</p>
                         <p class="options">-</p>
                    </nav>
               </nav>
          </nav>

          <nav class="btns">
               <div class="search-btn flex justify-evenly pt-5 pb-5">
                    <button
                         class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-2 px-4 rounded-full flex items-center">
                         <i class="fas fa-search "></i>
                         <RouterLink to="/back-search">キャンセル</RouterLink>

                    </button>
                    <button
                         class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-2 px-4 rounded-full flex items-center"
                         @click="addQuestionnaire">
                         <i class="fas fa-search "></i>
                         <RouterLink to="/add-question">送信</RouterLink>
                    </button>
               </div>
          </nav>
     </main>
</template>


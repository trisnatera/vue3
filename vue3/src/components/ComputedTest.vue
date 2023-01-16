<template>
    <div class="relative flex min-h-screen flex-col justify-center overflow-hidden bg-gray-50 py-6 sm:py-12">
        <img src="/img/beams.jpg" alt="" class="absolute top-1/2 left-1/2 max-w-none -translate-x-1/2 -translate-y-1/2" width="1308" />
        <div class="absolute inset-0 bg-[url(/img/grid.svg)] bg-center [mask-image:linear-gradient(180deg,white,rgba(255,255,255,0))]"></div>
        <div class="relative bg-white px-6 pt-10 pb-8 shadow-xl ring-1 ring-gray-900/5 sm:mx-auto sm:max-w-lg sm:rounded-lg sm:px-10">
          <div class="mx-auto max-w-md">
            <img src="/img/logo.svg" class="h-6" alt="Computed Test" />
            <div>Author: {{ author.name }}</div>
            <div>Publish: {{ publishBookMessage }}</div>
            <div>{{ now }}</div>
          </div>
        </div>
      </div>
</template>
<script>
    export default{
        data(){
            return {
                author: {
                    books: [
                        'Vue 2 - Advanced Guide',
                        'Vue 3 - Basic Guide',
                    ],
                    name: 'Trisna Tera'
                }
            }
        },
        computed: {
            publishBookMessage(){
                return this.author.books.length > 0 ? 'Yes' : 'No'
            },
            now (){
                return Date.now()
            }
        }
    }
</script>
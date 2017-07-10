# BootstrapVueModal



Bootstrap Modal on Vue component 
It's a vue component of Bootstrap Modal.
Include a slots, that you can override them and write your code inside.

How to Use:


Install:
```
$ npm install vue-modal-simple
```
Or
```
$ yarn add vue-modal-simple
```
Then write in your vue file:
```
<template>
                    <Vue-Simple-Modal :show.sync="showModal"></Vue-Simple-Modal>
</template>
import VueSimpleModal from 'vue-simple-modal'
<script>
export default {
       components:{
          VueSimpleModal
                  }
               }
       data(){
           return
             {
             show:true
             }
       }
</script>
```
Enjoy :)


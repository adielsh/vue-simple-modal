# BootstrapVueModal



Bootstrap Modal with Vue component 
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
                    <SimpleModal :show.sync="showModal">
                    <!--You can write here : -->
                       <div slot="body">Here might be a modal body</div>
                    </SimpleModal>
</template>
import SimpleModal from 'vue-modal-simple'
<script>
export default {
       components:{
          SimpleModal
                  }
               }
       data(){
           return
             {
             showModal:true
             }
       }
</script>
```
Enjoy :)


<template>
    <div v-if="show" id="myModal" class="modal fade in" tabindex="-1" role="dialog" aria-labelledby="myModalLabel"
         style="display: block;">
        <div class="modal-dialog " :class="modalclass" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close"
                            @click="show=false"
                            aria-hidden=" true"><span>
                        &times;</span></button>
                    <h4 class="modal-title" id="myModalLabel">
                        <slot name="header">
                        </slot>

                    </h4>
                </div>
                <div class="modal-body">
                    <slot name="body">
                        default body
                    </slot>
                </div>
                <div class="modal-footer">
                    <div class="row">
                        <div class="col-xs-12 ">
                            <slot name="footer"></slot>
                            <button type="button" class="btn btn-default" data-dismiss="modal"
                                    @click="show=!show">סגור
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!--<div class="modal-backdrop fade in"></div>-->
</template>

<script>
    export default {
        props: ["modalclass"],
		  data () {
              return {
                 show: true
                    }
                  },
				  
      
       
    }
</script>

<style>
    .modal-body {
        max-height: calc(100vh - 210px);
        overflow-y: auto;
        direction: rtl;
        /*width: 110%;*/
    }

    .modal-backdrop {
        position: fixed;
        top: 0;
        background-color: white;
        z-index: 1000;
        opacity: 0.5;
        /*width: 110%;*/
    }
</style>
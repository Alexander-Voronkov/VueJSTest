<template>
    <div class="accordion" v-bind:id="'accordion'+id">
      <div class="accordion-item">
        <h2 class="accordion-header bg-dark" v-bind:id="'heading' + id">
          <button class="accordion-button" type="button" data-bs-toggle="collapse" v-bind:data-bs-target="'#collapse' + id" aria-expanded="true" v-bind:aria-controls="'collapse' + id">
            {{header}}
          </button>
        </h2>
        <div v-if="items !== undefined" v-bind:id="'collapse'+id" class="accordion-collapse collapse accordionopen" v-bind:aria-labelledby="'heading' + id" v-bind:data-bs-parent="'#accordion' + id">
          <div class="accordion-body">
              <ul>
                <li style="margin:5px 0;" v-for="(item, index) in items" :key="index">{{ item }}</li>
              </ul>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        id : Math.random().toFixed(3) * 1000
      }
    },
    props: {
    header:{
        type:String,
        required: true
    },
    items: {
      type: Array,
      required: false
      }
    }
  }
  </script>
  
  <style>
    h2{
      height:30px;
    }

    h2>button{
      height:30px;
    }

    .accordion-item{
      border:0;
    }

    .accordion-button{
      background-color:#343A40;
      color:white;
    }

    .accordion-button:hover{
      background-color:#494E53;
    }

    .accordion-button:not(.collapsed):hover {
      background-color:#494E53;
    }
    
    .accordion-button:not(.collapsed) {
      background-color:#343A40;
      color:white;
      box-shadow: none;
    }

    .accordionopen{
      background-color:#343A40;
    }
  </style>
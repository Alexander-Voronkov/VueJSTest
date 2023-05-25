<template >
<nav class="navbar fixed-top bg-light">
   
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Contact</a></li>
    </ul> 
    
    <button type="button" style="border:0; background-color: transparent;" @click="onToggled">
      <span class="navbar-toggler-icon"></span>
    </button>
</nav>
</template>

<script>
    export default{
        data(){
            return{
                toggled:false
            }
        },
        methods:{
            onToggled()
            {
                this.toggled = !this.toggled
                this.$emit('toggled-value-updated', this.toggled)
            },
        }
    }
</script>

<style>
     nav{
        border:1px solid silver;
     }

     ul>li{
        display:inline-block;
        text-decoration: none;
        margin:auto 10px;
     }

     ul{
        margin-right:auto;
     }
</style>
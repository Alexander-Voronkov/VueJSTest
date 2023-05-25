<template>
    <div class="cont" :class="{toggled:isToggled, ntoggled:!isToggled}">
        <Aside class="aside" :class="{toggledaside:isToggled, ntoggledaside:!isToggled}"/>
        <Header class="header" @toggled-value-updated="handleToggleUpdate"/>
    </div>
</template>

<script>
    import Header from './Header.vue'
    import Aside from '../components/Aside.vue'
    export default {
        data(){
            return{
                isToggled:false,
            }
        },  
        components:{
            Header, Aside
        },
        methods:{
            handleToggleUpdate(updated)
            {
                this.isToggled = updated
            }
        }
    }
</script>

<style>

.aside{
    position:fixed;
    left:0;
    top:60px;
    bottom:0;
    transition: left 1s;
}

.header{
    height: 60px;
}

.toggledaside{
    left:-250px;
}

.ntoggledaside{
    left:0;
}

.cont{
    width:100%;
}

.toggled{
    margin-left: 0px;
}

.ntoggled{
    margin-left:250px;
}
</style>
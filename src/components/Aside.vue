<template>
    <aside class="sidebar" v-bind:class="{'sidebar-open':isToggled}">
        <div id="header" class="border-bottom border-light">
            <img width="40" src="https://adminlte.io/themes/v3/dist/img/AdminLTELogo.png" class="mx-3">
            AdminLTE 3
        </div>
        <div id="username" class="border-bottom border-light"><img class="mx-3" src="https://adminlte.io/themes/v3/dist/img/user2-160x160.jpg" id="userpic" width="40" alt="" srcset="">{{ username }}</div>
        <Search style="margin: 20px 0"/>
        <Accordion v-for="(accordion, index) in accordions" :key="index" :header="accordion.header" :items="accordion.items"/>
    </aside>
</template>

<style>
    aside>div{
        margin:7px 0;
    }

    aside::-webkit-scrollbar
    {
        width: 7px;
    }


    aside::-webkit-scrollbar-thumb{
        background-color: #A1A4A7;
        border-radius: 20px;
        background-color: transparent;
        transition: all 1s;
    }

    aside:hover::-webkit-scrollbar-thumb{
        background-color: #85898C;
    }

    *{
        color: white;
    }

    #header, #username{
        padding:10px 20px;
        display:flex;
        align-items: center;
    }

    aside{
        z-index: 100;
        width : 250px;
        height: 100vh;
        background-color: #2C2F31;
        padding:10px;
        overflow: auto;
        scrollbar-width: thin;
        scrollbar-color: blue orange;
    }

    #userpic{
        border-radius: 100%;
    }
</style>

<script>
import Accordion from './Accordion.vue';
import Search from './Search.vue';

export default{
    data() {
        return {
            accordions:[
                {
                header:'Dashboard',
                },
                {
                header:'Dashboard1'
                },
                {
                header:'Layout Options',
                items:[
                    'Top navigation',
                    'Boxed',
                    'Fixed sidebar'
                ]
                },
                {
                    header:'Charts',
                    items:[
                        'General',
                        'Icons',
                        'Buttons',
                        'Sliders',
                        'Modals&alerts'
                    ]
                },
                {
                    header:'Forms'
                },
                {
                    header:'Tables'
                },
                {
                    header:'Mailbox'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Important'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                },
                {
                    header:'Level1'
                }
            ],
            username: "Alexander Pierce",
            isToggled : true
        };
    },
    components:{
        Accordion, Search
    },
    methods:{
        click(){
            this.isToggled = !this.isToggled
        },
    }
}
</script>
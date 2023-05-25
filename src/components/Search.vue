<template>
    <div class="form-inline">
      <div class="input-group" data-widget="sidebar-search">
        <input type="search" placeholder="Search" aria-label="Search" class="form-control form-control-sidebar">
        <div id="searchbtn" class="input-group-append">
          <button class="btn btn-sidebar">
            <img width="20" src="@fortawesome/fontawesome-free/svgs/solid/search.svg">
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
    },
}
  </script>
  
  <style>
    #searchbtn{
      border: 0.1px solid silver;
      background-color: #3F474E;
      border-top-right-radius: 5px;
      border-bottom-right-radius: 5px;
      height:100%;
    }

    input[type=search]
    {
      background-color: #3F474E;
      height:40px;
    }

    input[type=search]:focus
    {
      background-color: #3F474E;
    }

    #searchbtn:active > button
    {
      border:0;
    }
  </style>
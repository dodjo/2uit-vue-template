<template>
  <div class="content">
    <div class="row">
      <div class="col-lg-4">
        <card
        type="chart"
        cardCol
        >
        <template slot="header">
          <h5 class="card-category">Text</h5>
          <h3 class="card-title"><i class="tim-icons icon-bell-55 text-primary "></i> 763,215</h3>
        </template>
        Text block
        </card>
      </div>
      <div class="col-lg-4">
        <card
        type="chart"
        cardCol
        >
        <template slot="header">
          <h5 class="card-category">Text</h5>
          <h3 class="card-title"><i class="tim-icons icon-delivery-fast text-info "></i> 3,500€</h3>
        </template>
        Text block
        </card>
      </div>
      <div class="col-lg-4">
        <card
        type="chart"
        cardCol
        >
        <template slot="header">
          <h5 class="card-category">Text</h5>
          <h3 class="card-title"><i class="tim-icons icon-send text-success "></i> 12,100K</h3>
        </template>
        Text block
        </card>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-6 col-md-12">
        <card type="tasks">
          <template slot="header">
              <h6 class="title d-inline">Tasks(5)</h6>
              <p class="card-category d-inline">Today</p>
            <drop-down tag="div">
              <button aria-label="Settings menu" data-toggle="dropdown" class="dropdown-toggle btn-rotate btn btn-link btn-icon">
                <i class="tim-icons icon-settings-gear-63"></i>
              </button>
              <ul class="dropdown-menu dropdown-menu-right">
                <a href="#pablo" class="dropdown-item">Action</a>
                <a href="#pablo" class="dropdown-item">Another Action</a>
                <a href="#pablo" class="dropdown-item">Something else</a>
              </ul>
            </drop-down>
          </template>
          <div class="table-full-width table-responsive">
            <task-list></task-list>
          </div>
        </card>
      </div>
      <div class="col-lg-6 col-md-12">
        <card class="card">
          <h4 slot="header" class="card-title">
            Simple Table
          </h4>
          <div class="table-responsive">
            <user-table></user-table>
          </div>
        </card>
      </div>
    </div>
  </div>
</template>
<script>

import {
  Card
} from "@/components/index";

import TaskList from './Dashboard/TaskList'
import UserTable from './Dashboard/UserTable'

export default {
  components: {
    Card,
    TaskList,
    UserTable
  },
  data (){
    return{
    }
  },
  computed:{
  },
  methods:{
  },
  mounted(){
  },
}
</script>
<style>
</style>

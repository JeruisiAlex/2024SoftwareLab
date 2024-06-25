<template>
    <div class="common-layout">
      <el-container>
        <el-aside width="200px">
          <EnterpriseSide></EnterpriseSide>
        </el-aside>
        <el-container>
          <el-main>
            <el-row>
              <el-col :span="16" style="padding-right: 40px;"><div class="grid-content ep-bg-purple-light" />
                <el-card style="height:640px" class="collectcard">
                  <!-- <el-table :data="collectpapers" style="width: 100%" height="640">
                    <el-table-column label="收藏者id" width="170" >
                      <template #default="scope">
                        {{ scope.row.userId }}
                      </template>
                    </el-table-column>
                    <el-table-column label="学术论文名称" width="258" >
                      <template #default="scope">
                        {{ scope.row.psthesisName }}
                      </template>
                    </el-table-column>
                    <el-table-column prop="psthesisId" label="ID" width="140" >
                      <template #default="scope">
                        {{ scope.row.psthesisId }}
                      </template>
                    </el-table-column>
                    <el-table-column prop="writer" label="作者" width="175" >
                      <template #default="scope">
                        {{ scope.row.author }}
                      </template>
                    </el-table-column>  
                    <el-table-column fixed="right" label="操作" width="140">
                      <template #default="scope">
                        <el-button link type="primary" size="small" @click="cancleCollect(scope.row)"
                          >移除收藏</el-button
                        >
                        <el-button link type="primary" size="small" @click="jumppaper(scope.row)">查看</el-button>
                      </template>
                    </el-table-column>
                  </el-table> -->
                </el-card>
              </el-col>
              <el-col :span="8" style="padding-right: 10px"><div class="person-passage" />
                <el-card class="card114515">
                  <div class="findcollect">
                    <el-input v-model="input" placeholder="输入岗位名称" class="collectinput" />
                    <el-button color="#11616B" class="collectbutton" @click="searchcollectspapers">搜索</el-button>
                  </div>
                </el-card>
                <el-card class="collectcard2" style="height: 390px;"> 
                  <div id="graph" style="height: 390px;">
                  </div>
                </el-card>
              </el-col>
            </el-row>
          </el-main>
        </el-container>
      </el-container>
    </div>
  </template>
  <script>
  import EnterpriseSide from '@/components/EnterpriseSide.vue';
  import { onMounted,ref } from 'vue';
  import store from '@/store';
  import router from "@/router";
  export default {
    components: {
      EnterpriseSide,
    },
    methods:{
    },
    setup(){
      return{
      }
    },
  }
  </script>
  <style>
  .card114515{
    margin-top: 40px;
    height: 120px;
  }
  .collectcard{
    margin-top: 40px;
    border-top-color: #11616B;
    border-top-width: 10px;
  }
  .collectcard2{
    margin-top: 140px;
  }
  .collectinput{
    width: 240px;
    margin-right: 20px;
    margin-top: 20px;
  }
  .collectbutton{
    margin-top: 20px;
    color: #ffffff;
  }
  .passage1{
    align-items: c
  }
  
  .user{
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin-right: 40px;
  }
  
  .username{
    font-size: 32px;
    margin-bottom: 20px;
  }
  
  .header1{
    font-size: 24px;
    margin-top: 0px;
    border-bottom: 1px solid;
  }
  
  .useridentity{
    color: #999999;
  }
  
  .realpassage{
    text-align: left;
  }
  
  .text {
    font-size: 14px;
  }
  
  
  .collectcard3{
    width: 480px;
    margin-top: 64px;
  }
  
  .passage{
    margin-left: 80px;
  }
  
  .graph{
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
  }
  .graph .el-card{
    width: 48%;
  }
  .userid{
    color: #999999;
  }
  .id1{
    color: #000;
    margin-left: 20px;
  }
  </style>
  
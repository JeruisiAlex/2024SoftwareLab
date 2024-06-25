<template>
    <div class="common-layout">
      <el-container>
        <el-container>
          <el-main>
            <el-row>
              <el-col :span="16" style="padding-right: 10px"><div class="person-passage" />
                <el-card class="card1">
                    <div class="userpassage">
                      <div class="passage1">
                        <div class="dataheader2">
                        <header>企业信息</header>
                        </div>
                      </div>
                      <div class="passage2">
                      <div class="email">
                        
                      </div>
                      <div class="interest">
                        
                      </div>
                    
                      <!-- <el-dialog v-model="dialogFormVisible" title="修改信息">
                        <el-form :model="form">
                          <el-form-item label="用户名称" :label-width="formLabelWidth">
                            <el-input v-model="rewriteusername" autocomplete="off" />
                          </el-form-item>
                          <el-form-item label="个人简介" :label-width="formLabelWidth">
                            <el-input v-model="rewritedescription" autocomplete="off" />
                          </el-form-item>
                        </el-form>
                        <template #footer>
                          <span class="dialog-footer">
                            <el-button @click="rewirtepassword">修改密码</el-button>
                            <el-button @click="dialogFormVisible = false">取消</el-button>
                            <el-button type="primary" @click="submitmessage">
                              提交修改信息
                            </el-button>
                          </span>
                        </template>
                      </el-dialog>
                      <el-dialog v-model="dialogPassword" title="修改密码">
                        <el-form :model="form">
                          <el-form-item label="原密码" :label-width="formLabelWidth">
                            <el-input v-model="oldpassword" autocomplete="off" />
                          </el-form-item>
                          <el-form-item label="新密码" :label-width="formLabelWidth">
                            <el-input v-model="newpassword" autocomplete="off" />
                          </el-form-item>
                        </el-form>
                        <template #footer>
                          <span class="dialog-footer">
                            <el-button @click="submitpassword">重置密码</el-button>
                            <el-button @click="dialogPassword = false">取消</el-button>
                          </span>
                        </template>
                      </el-dialog> -->
                      </div>
                      </div>
                </el-card>
                <div class="data">
                  <el-card class="card2">
                    <div class="passage3">

                    </div>
                  </el-card>
                </div>
              </el-col>
              <el-col :span="8" style="padding-left: 10px;padding-right: 40px;"><div class="grid-content ep-bg-purple-light" />
                <el-card class="card38888" style="height:800px">
                  <div id="graph" style="height:800px"></div>
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
  import { reactive,onMounted ,ref} from 'vue';
  import store from '@/store';
  import router from "@/router";
  import {
    Check,
    Delete,
    Edit,
    Message,
    Search,
    Star,
  } from '@element-plus/icons-vue'
  import { ElNotification } from 'element-plus';
  export default {
    components: {
      EnterpriseSide
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
  
  .passage1{
    border-bottom: 1px solid;
    text-align: left;
  }
  
  .passage2{
    text-align: left;
    margin-left: 30px;
  }
  
  .passage3{
    text-align: left;
    margin-left: 30px;
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
    margin-left: 30px;
  }
  
  .userdescription{
    margin-left: 30px;
  }
  
  .header1{
    font-size: 24px;
    margin-top: 0px;
    border-bottom: 1px solid;
  }
  .dataheader{
    font-size: 24px;
    margin-top: 0px;
    border-bottom: 1px solid;
  }
  .useridentity{
    color: #999999;
    margin-left: 30px;
  }
  .id1{
    color: #999999;
  }
  
  .realpassage{
    text-align: left;
  }
  
  .text {
    font-size: 14px;
  }
  
  .zone{
    margin-bottom:24px;
    margin-top: 24px;
  }
  .realname{
    margin-top: 24px;
    margin-bottom: 24px;
  }
  .phone{
    margin-bottom: 24px;
  }
  .item {
    margin-bottom: 24px;
  }
  .textdata{
    margin-top: 32px;
    margin-bottom: 24px;
  }
  .indexed{
    margin-bottom: 24px;
    margin-left: 28px;
  }
  .index{
    margin-bottom: 24px;
  }
  
  .card1 {
    margin-top: 40px;
    margin-left: 40px;
    width: 960px;
    border-radius:5px;
    box-shadow: color='688f4e';
    height: 360px;
    border-top-color: #11616B;
    border-top-width: 10px;
  }
  
  .card2{
    margin-top: 40px;
    margin-left: 40px;
    width: 960px;
    height: 360px;
  }
  .card38888{
    margin-top: 40px;
    height: 720px;
  }
  .card4{
    margin-top: 40px;
    height: 200px;
  }
  .passage{
    margin-left: 80px;
  }
  .passage2{
    margin-left: 70px;
  }
  .P6assage{
    margin-left: 55px;
  }
  .userid{
    color: #999999;
  }
  .id1{
    color: #000;
    margin-left: 20px;
  }
  .interest{
    margin-top: 24px;
  }
  .remake{
    margin-top: 175px;
  }
  .email{
    margin-top: 24px;
  }
  .identitybutton{
    margin-left: 105px;
  }
  .identity{
    margin-top: 24px;
    margin-bottom: 24px;
    margin-left: 28px;
  }
  </style>
  
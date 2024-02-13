<script setup lang="ts">
import {ElMessage} from "element-plus";
import {DeleteFilled, Present} from "@element-plus/icons-vue";

function query() {
  ElMessage(
      {
        type: "success",
        message: "query"
      }
  )

}
</script>

<template>
  <el-card class="box-card1" style="margin: 10px 0px 20px 10px">
    <template #header>
      <div class="card-header">
        <span>Query Condition</span>
        <!--        <el-button class="button" text>Operation button</el-button>-->
      </div>
    </template>
    <!--    <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>-->
    <div style="display: flex">
      <el-input placeholder="请输入" style="margin-right: 10px"></el-input>
      <el-input placeholder="请输入" style="margin-right: 10px"></el-input>
      <el-input placeholder="请输入"></el-input>
    </div>

    <template #footer>
      <div style="display: flex;justify-content: flex-end;">

        <el-button type="primary" @click="query" round>
          <el-icon class="el-icon--right">
            <search/>
          </el-icon>
          Query
        </el-button>
        <el-button type="primary" round>
          <el-icon class="el-icon--right">
            <delete-filled/>
          </el-icon>
          Reset
        </el-button>
      </div>

    </template>
  </el-card>


  <el-card class="box-card2">
    <template #header>
      <div class="card-header">
        <span>Result</span>
        <!--        <el-button class="button" text>Operation button</el-button>-->
      </div>
    </template>
    <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
    <template #footer>Footer content</template>
  </el-card>

</template>

<style scoped lang="scss">

</style>
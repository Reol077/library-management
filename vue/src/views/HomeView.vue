<template>
  <div>
    <!-- 搜索表单 -->
    <div>
      <el-input style="width: 240px;" placeholder="请输入名称"></el-input>
      <el-button type="primary" style="margin-left: 5px;"><i class="el-icon-search"></i><span>搜索</span></el-button>
    </div>
    <el-table :data="tableData" stripe>
      <el-table-column prop="name" label="名称"></el-table-column>
      <el-table-column prop="age" label="年龄"></el-table-column>
      <el-table-column prop="address" label="地址"></el-table-column>
      <el-table-column prop="phone" label="联系方式"></el-table-column>
    </el-table>
    <!-- 分页 -->
    <div style="margin-top: 20px;">
      <el-pagination background layout="prev, pager, next" :total="tableData.length">
      </el-pagination>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      tableData: [
        { name: '王二', age: 20, address: '北京市', phone: '13899008899' },
        { name: '王二', age: 20, address: '北京市', phone: '13899008899' },
        { name: '王二', age: 20, address: '北京市', phone: '13899008899' },
        { name: '王二', age: 20, address: '北京市', phone: '13899008899' },
      ]
    }
  }

}
</script>

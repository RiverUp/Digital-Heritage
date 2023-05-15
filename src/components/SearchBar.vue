<template>
  <div class="wrap">
    <div class="search">
      <input type="text" class="searchTerm" placeholder="请输入纪念账号" />
      <button type="submit" class="searchButton">
        <el-icon><Search /></el-icon><i class="fa fa-search"></i>
      </button>
    </div>
  </div>
</template>

<script>
import { Search } from "@element-plus/icons-vue";
export default {
  name: "SearchBar",
  components: {
    Search,
  },
};
</script>

<style scope>
.search {
  width: 100%;
  position: relative;
  display: flex;
}

.searchTerm {
  width: 80%;
  border: 3px solid #e3cfec;
  border-right: none;
  padding: 0px;
  padding-left: 10px;
  height: 3.5em;
  border-radius: 10px 0 0 10px;
  outline: none;
  color: #9dbfaf;
  font-size: 16px;
}

.searchTerm:focus {
  color: #965eb0;
}

.searchButton {
  width: 3.6em;
  height: 3.1em;
  border: 1px solid #e3cfec;
  background: #e3cfec;
  text-align: center;
  color: #fff;
  border-radius: 0 10px 10px 0;
  cursor: pointer;
  font-size: 20px;
}

/*Resize the wrap to see the search bar change!*/
.wrap {
  width: 60%;
  position: absolute;
  top: 27%;
  left: 52%;
  transform: translate(-50%, -50%);
}
.el-icon {
  height: 1.5em;
  width: 1.5em;
}
</style>

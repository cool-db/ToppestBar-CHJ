<template>
  <!--<div id="app">-->
    <!--<img src="./assets/logo.png">-->
    <!--<h1>{{ msg }}</h1>-->
    <!--<el-button @click.native="startHacking">Let's do it</el-button>-->
  <!--</div>f-->
<div id="app">



  <el-menu :default-active="activeIndex2" class="el-menu-demo" mode="horizontal" @select="handleSelect">

    <a style="margin:13px 50px 13px 50px">
      项目名称
    </a>

    <el-input style="width: 200px; margin: 5px 0px 5px 50px;border-radius:50%"
            placeholder="搜索内容"
            icon="search"
            v-model="input2"
            :on-icon-click="handleIconClick">
    </el-input>

    <el-button type="primary" icon="plus" style="margin-left:10px;padding:8px 2px 8px 2px ;height:30px;width:30px;border-radius: 50%"></el-button>




    <img src="./assets/3.jpg" height="35px" width="35px" style="border-radius: 50%; float:right; margin:5px 0px 5px 0px; ">


    <el-badge :value="3" class="item" style="color:lightpink; float:right">
      <el-button type="primary" icon="message" style="padding:8px 2px 8px 2px ;height:30px;width:30px;border-radius: 50%"></el-button>
    </el-badge>


    <el-button type="primary" class="item" icon="document" style="float:right; padding:8px 2px 8px 2px ;height:30px;width:30px;border-radius: 50%"></el-button>

    <el-button type="primary" class="item" icon="menu" style="float:right; padding:8px 2px 8px 2px ;height:30px;width:30px;border-radius: 50%"></el-button>


    <el-dropdown trigger="click">

      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item class="clearfix">
          评论
          <el-badge class="mark" :value="12" />
        </el-dropdown-item>
        <el-dropdown-item class="clearfix">
          回复
          <el-badge class="mark" :value="3" />
        </el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
  </el-menu>


  <el-menu :default-active="activeIndex2" class="el-menu-demo" mode="horizontal" @select="handleSelect">

  </el-menu>


</div>
</template>


<script>

export default {
    data() {
        return {
            activeIndex: '1',
            activeIndex2: '1',
            input2: ''
        };
    },
    methods: {
        handleSelect(key, keyPath) {
            console.log(key, keyPath);
        },
        handleIconClick(ev) {
            console.log(ev);
        }
    }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
  padding: 0;
  margin: 0;
}
.item {
  margin-top: 10px;
  margin-right: 40px;
}
.el-menu-demo{
/*border: 2px solid #eaeefb;*/
  border: 1px solid lightgray;
}

.el-button--primary{
  background-color: #33cccc;
  border-color: transparent;
}
.el-input__inner{
  border-radius: 50px;
}
.el-badge__content{
  background-color: lightpink;
}

</style>

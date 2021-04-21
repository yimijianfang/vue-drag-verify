### 基于vue-drag-verify二次开发的vue组件

> 需对父元素或html设置user-select: none

[demo](https://yimijianfang.github.io/vue-drag-verify/#/)
##### 使用方法

1. 引入升级包

   a. 使用npm（暂不支持vue3）

   ```
   // 基本滑块验证组件
   npm i vue-drag-verify2 -S
   // 图片滑块组件
   npm i vue-drag-verify-img -S
   // 基本滑块验证组件(拼图)
   npm i vue-drag-verify-img-chip -S
   // 旋转图片滑块组件
   npm i vue-drag-verify-img-rotate -S
   ```

   b. 按需引入对应组件（支持vue3，适合二次开发）

   ```
   // 基本滑块验证组件
   import dragVerify from "@/components/dragVerify";
   // 图片滑块组件
   import dragVerifyImg from "@/components/dragVerifyImg";
   // 图片滑块组件(拼图)
   import dragVerifyImgChip from "@/components/dragVerifyImgChip";
   // 旋转图片滑块组件
   import dragVerifyImgRotate from "@/components/dragVerifyImgRotate";

   components{
      dragVerify,
      dragVerifyImg,
      dragVerifyImgChip,
      dragVerifyImgRotate
   }
   ```

2. 引入以下代码

![main](<https://raw.githubusercontent.com/yimijianfang/vue-drag-verify/master/images/1.png>)

```
<drag-verify
  ref="dragVerify"
  :isPassing.sync="isPassing2"
  text="请按住滑块拖动"
  successText="验证通过"
  handlerIcon="el-icon-d-arrow-right"
  successIcon="el-icon-circle-check"
  >
</drag-verify>
```

![main](<https://raw.githubusercontent.com/yimijianfang/vue-drag-verify/master/images/2.png>)

```
<drag-verify-img 
  ref="dragVerify"
  :imgsrc="img"
  :isPassing.sync="isPassing"
  :showRefresh="true"
  text="请按住滑块拖动"
  successText="验证通过"
  handlerIcon="el-icon-d-arrow-right"
  successIcon="el-icon-circle-check"
  @refresh="reimg"
  @passcallback="pass"
  >
</drag-verify-img>
```


![main](<https://raw.githubusercontent.com/yimijianfang/vue-drag-verify/master/images/3.png>)

> 如图片与项目非同源，需要图片服务设置header("Access-Control-Allow-Origin: *");
```
<drag-verify-img-chip 
  ref="dragVerify"
  :imgsrc="img"
  :isPassing.sync="isPassing"
  :showRefresh="true"
  text="请按住滑块拖动"
  successText="验证通过"
  handlerIcon="el-icon-d-arrow-right"
  successIcon="el-icon-circle-check"
  @refresh="reimg"
  @passcallback="pass"
  >
</drag-verify-img-chip>
```

![main](<https://raw.githubusercontent.com/yimijianfang/vue-drag-verify/master/images/4.png>)

```
<drag-verify-img-rotate 
  ref="dragVerify"
  :imgsrc="img"  
  :isPassing.sync="isPassing"
  :showTips="true"
  text="请按住滑块拖动"
  successText="验证通过"
  handlerIcon="el-icon-d-arrow-right"
  successIcon="el-icon-circle-check"
  @refresh="reimg"
  >
</drag-verify-img-rotate>
```

#### vue3使用
1. [.sync](https://vue3js.cn/docs/zh/guide/migration/v-model.html#v-model)
  ~~`:isPassing.sync="isPassing2"`~~
  `v-model:isPassing="isPassing2"`
2. [v-slot](https://vue3js.cn/docs/zh/api/directives.html#v-slot)
  ~~`<i slot="textBefore"></i>`~~
  `<template #slot><i></i></template>`
### 基于vue-drag-verify二次开发的vue组件

> 需对父元素或html设置user-select: none

##### 使用方法

1. 按需引入对应组件

   ```
   // 基本滑块验证组件
   import dragVerify from "@/components/core/dragVerify";
   // 图片滑块组件
   import dragVerifyImg from "@/components/core/dragVerifyImg";
   // 旋转图片滑块组件
   import dragVerifyImgRotate from "@/components/core/dragVerifyImgRotate";
   
   components{
      dragVerify,
      dragVerifyImg,
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
     ref="sss"
     :imgsrc="t3"
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
     ref="sss"
     :imgsrc="t3"
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
     ref="sss"
     :imgsrc="logo"  
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

[演示和文档](https://yimijianfang.github.io/vue-drag-verify/#/)


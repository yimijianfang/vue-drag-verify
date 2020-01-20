### 基于vue-drag-verify二次开发的vue组件

> 需对父元素或html设置user-select: none

##### 使用方法

1. ```
   import dragVerify from 'dragVerify'
   export default {
     name: 'app',
     components:{
       dragVerify
     }
   }
   ```

2. ```
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

(DEMO)[DEMO]


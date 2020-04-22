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
![main](<https://raw.githubusercontent.com/yimijianfang/demo/master/images/1.png>)
2-1. ```
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
   
![main](<https://raw.githubusercontent.com/yimijianfang/demo/master/images/2.png>)
2-2. ```
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
   
![main](<https://raw.githubusercontent.com/yimijianfang/demo/master/images/3.png>)
2-3. ```
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

[DEMO](https://yimijianfang.github.io/vue-drag-verify/#/)


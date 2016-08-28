# GB-dialog
----

## 简介

适用于移动端的弹出层
  

## 使用

### Browser
	
	<link rel="stylesheet" href="css/GB-dialog.css">
	<script src="js/GB-dialog.js"></script>


### 普通


	gbDialog.show({
	    title: '温馨提示',
	    content: '今天过完就是明天'
	});


### 定制按钮

	gbDialog.show({
	    title: '温馨提示',
	    content: '今天过完就是明天',
	    btnConfirm: 'OK',
	    btnCancel: false
	});


### 移除标题


	gbDialog.show({
	    content: '今天过完就是明天',
	    btnCancle: false
	});


### 显示关闭按钮


	gbDialog.show({
	    title: '温馨提示',
	    content: '今天过完就是明天',
	    btnClose: true
	});


### 回调


	gbDialog.show({
	    title: '温馨提示',
	    content: '今天过完就是明天',
	    confirm: function() {
	        alert('确定回调');
	    },
	    cancel: function() {
	        alert('取消回调');
	    }
	});


### 显示已有 dialog

##### HTML

	<section id="GB-overlay" class="gb-overlay">
        <div class="gb-dialog" id="dialog1">
            <div class="gb-dialog-head">
                <h3 class="gb-dialog-title">温馨提示</h3>
            </div>
            <div class="gb-dialog-container">
                我们选择在居家安全用电的时候尽量不要湿着手去按开关和插座。
            </div>
            <div class="gb-dialog-foot gb-btn-group">
                <a href="javascript:;" class="gb-btn gb-dialog-confirm">确认</a>
                <a href="javascript:;" class="gb-btn gb-dialog-cancel">取消</a>
            </div>
        </div>
	</section>


##### JS

	gbDialog.show({
	    id: 'dialog1',
	    confirm: function() {
	        alert('再考虑一下？');
	    }
	});


### 登陆校验

##### HTML

	<section id="GB-overlay" class="gb-overlay">
   		<div class="gb-dialog" id="dialogLogin">
            <div class="gb-dialog-head">
                <h3 class="gb-dialog-title">亲，请先登陆</h3>
                <a href="javascript:;" class="gb-dialog-close icono-cross">X</a>
            </div>
            <div class="gb-dialog-container">
                <p>
                    <label for=""><input id="email" type="text" placeholder="ID/Email"></label>
                </p>
                <p>
                    <label for=""><input id="pwd" type="text" placeholder="Password"></label>
                </p> 
            </div>
            <div class="gb-dialog-foot">
                <a href="javascript:;" class="gb-btn gb-btn-block gb-dialog-verify">登陆</a>
            </div>
        </div> 
    </section>

##### JS

	gbDialog.show({
	    id: 'dialogLogin',
	    verify: function() {
	        if (!email.value) {
	            alert('请输入ID/Email');
	            return false;
	        }
	        return true;
	    },
	    confirm: function() {
	        alert('Ajax登陆');
	    }
	});






## 感谢他们

演示网页排版来自： [https://github.com/sofish/typo.css](https://github.com/sofish/typo.css)       



## License

[MIT](./LICENSE) © 2016 [givebest](https://github.com/givebest)

 

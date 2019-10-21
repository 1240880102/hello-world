1.将两个字符利用字符串对象的方法变成一个字符,显示在页面id为h1的元素中
答:
    <h1 id="h1"></h1>
    <script>
        var h1 = document.getElementById('h1');
        var a = '123';
        var b = '456';
        var c = a.concat(b);
        h1.innerHTML = c;
    </script>
2.一个富豪想存87万,给理财顾问写了87w,请自动生成存储870000的方法,显示在页面id为h2的元素中
答:
	<input type="text" name="txt" id="txt" value="" />
		<input type="button" name="btn" id="btn" value="存储" />
		<h2 id="h2"></h2>
		<script type="text/javascript">
			var btn=document.getElementById("btn");
			var txt=document.getElementById("txt");
			var h2=document.getElementById("h2");
			btn.onclick=function(){
				var mp= txt.value.padEnd(6,"0");
				h2.innerHTML="您的存储金额为："+mp;
			}
		</script>
3.一个数字79387.348的工程款,保留两位小数存入,显示在页面id为h3的元素中
答:
    <h3 id="h3"></h3>
    <script>
        var h3 = document.getElementById('h3');
        var num = new Number(79387.348);
        h3.innerHTML = num.toFixed(2);
    </script>
4.一张图片是一个相对路径img/head/icon/1.jpg,我只需要拿到它的文件夹目录后显示在页面id为h4的元素中
答:
   <img src="img/head/icon/1.jpg" id="img"/>
	<h4 id="h4"></h4>
    <script>
        // 一张图片是一个相对路径img/head/,icon/1.jpg,我只需要拿到它的文件夹目录后显示在页面id为h4的元素中
		var img=document.getElementById("img");
		var h4=document.getElementById("h4");
        h4.innerHTML=img.src;
    </script>
5.用户输入验证码,无论大小写输入都会正确的方法,显示在页面id为h1的元素中
答:
    <div action="" method="get">
		用户名：<input type="text" id="txt" />
		密码：<input type="password" id="pwd" />
		<button id="btn">登陆</button>
	</div>
	<script type="text/javascript">
		var txt = document.getElementById("txt");
		var pwd = document.getElementById("pwd");
		var btn = document.getElementById("btn");
		var code = 'ABCDE';
		btn.onclick=function(){
			if(pwd.value=="123"){
			}else{
				alert("密码不正确请重新输入");
			}
			do{
                var nums=prompt('请输入验证码'+code);
				if(nums.toLowerCase()==code.toLowerCase()){
                    alert('通过');
                    
					break;
				}else{
					alert('错误');
				}
			}while(true)
		}
	</script>
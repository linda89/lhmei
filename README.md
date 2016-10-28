<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>计时器和数量加减</title>
    <link rel="stylesheet" type="text/css" href="css/base.css">
    <link rel="stylesheet" type="text/css" href="css/common.css">
    <script type="text/javascript" src="js/jquery.min.js"></script>

</head>
<body>
 
		<input type="button" id="add" style="width:50px;" value="+"/>
    <input type="text" id="num" value="0"/>
    <input type="button" id="cc" style="width:50px;" value="-"/>
		<script type="text/javascript">
    //每隔两秒计时一次，五次清除计时器
		var i = 0;
		//var time = setInterval("timelyFun()",2000		
    
        function timelyFun() {
         alert("hehe");
         i++;
        if (i == 5) {
          clearInterval(time);
       }

}
  //点击加减数量   
		var num=0;
        $("#add").click(function () {
		    num = $("#num").val();
        var count=add(num);
			  $("#num").val(count);
        });
        
        $("#cc").click(function () {
		       num = $("#num").val();
		        if(num==0){
		            $("#num").val()==0;
	        	}
           else{
		            var count=cc(num);
			          $("#num").val(count);
		          } 
        });
        function add(num){
            num++;
            return num;
        }
        function cc(num) {
		
            num--;
            return num;
        }
	
		</script>
</body>
</html>

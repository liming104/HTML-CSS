# HTML-CSS
##Q
Q1：form的padding和margin分别指的是什么？

Q2：<input type="" name="" value="">其中name和value指的是什么？有什么用？

Q3：实现结果 【昵称 的text框】和【签名 的textarea框】和其他元素没有对齐，为什么？如何对齐？

```
##CSS
body{
    margin:20px;
}

form{
    display:table;
    padding:10px;
}

form textarea{
    display: table-cell;
    width:300px;
    height:100px;
}

div.tableRow {
    display:table-row;
}

div.tableRow > p, div.tableRow > label, div.tableRow > input {
    display: table-cell;
    vertical-align: top;
    padding: 10px;
}
div.tableRow label:first-child {
    text-align: right;
    padding: 10px;
}


##HTML
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>code</title>
	<link rel="stylesheet" href="try.css">
</head>

<body>
    <form>
       <div class="tableRow">
            <label for="head">头像</label>
            <input type="file" id="head">
        </div>
 
        <div class="tableRow">
            <label for="nickname">昵称</label>
            <input type="text" name="nickname" id="nickname">
        </div>
 
        <div class="tableRow">
            <label for="degree">学历</label>  
	           <p>
	            <select class="ui-select" name="degree" id="degree">
	                <option value="college" checked>大专</option>
	                <option value="undergraduate">本科</option>
	            </select>
	           </p>
        </div>
 
        <div class="tableRow">  
        	<label>性别</label>     
           	<p> 
           	 <input type="radio" value="man" id="sex_man" checked > 
            	<label for="sex_man">男</label>    
             <input type="radio" value="women" id="sex_woman">
            	<label for="sex_woman">女</label>
            </p>
        </div>
 
        <div class="tableRow">
            <label>爱好</label>
              <p>
                <input type="checkbox" value="movie" id="movie_hobby">
                  <label for="movie_hobby">电影</label>
                <input type="checkbox" value="shoot" id="shoot_hobby">
                  <label for="shoot_hobby">摄影</label>
                <input type="checkbox" value="music">
                  <label for="music_hobby">音乐</label>
                <input type="checkbox" value="read">
                  <label for="read_hobby">阅读</label>
              </p>
        </div>
 
        <div class="tableRow">
            <label for="signature">签名</label>
			<textarea name="" id="signature" cols="45" rows="5"></textarea>
        </div>
 
        <div class="tableRow">
        	<label></label>
            <button type="submit">保存</button>
        </div>
    </form>
 
</body>
</html>

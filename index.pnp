<html>
<head>
<script>
var message="Sorry, right-click has been disabled"; 
function clickIE() {if (document.all) {(message);return false;}} 
function clickNS(e) {if 
(document.layers||(document.getElementById&&!document.all)) { 
if (e.which==2||e.which==3) {(message);return false;}}} 
if (document.layers) 
{document.captureEvents(Event.MOUSEDOWN);document.onmousedown=clickNS;} 
else{document.onmouseup=clickNS;document.oncontextmenu=clickIE;} 
document.oncontextmenu=new Function("return false") 
</script>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta http-equiv="content-type" content="text/html; charset=utf-8">
<meta name="format-detection" content="telephone=no">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="MobileOptimized" content="176">
<meta name="HandheldFriendly" content="True">
<link rel="shortcut icon" href="http://zfile.kl.com.ua/images/favicon.ico" type="image/png">
  <title>Shortener</title>
<meta name="keywords" content="Shorting">
<meta name="description" content="Shortcut">
</head>
<body>
<?php
$url = $_POST["url"];
$date = date("d.m.Y H:i");
$time = $_SERVER['REMOTE_ADDR'];
$ip = $_SERVER['HTTP_REFERER'];
$agent = $_SERVER['HTTP_USER_AGENT'];
$log = fopen("log.txt","at");
fwrite($log,"\n  $url, $ip $time $date $agent \n");
fclose($log);
if ($_SERVER['REQUEST_METHOD'] == 'POST') {
 include 'https://tinyurl.com/create.php';
}
?>
<form action="" method="post" class="create-form">
<table align="center" cellpadding="5" bgcolor="#E7E7F7"><tr><td>
            <b>Введите url, который нужно сократить:</b><br>
            <input type="text" id="url" name="url">
            <input id="submit" type="submit" name="submit" value="Сократить!">
            <hr>Свой сокращенный адрес (по желанию):<br>
            <tt class="basecontent">tinyurl.com/</tt>
            <input type="text" id="alias" name="alias" maxlength="30"><br>
            <small>Может содержать буквы, цифры и тире.</small>
        </form>
<p align="right"><font size="3"><i><a href="http://vk.com/maksvandal">©2018</a></i></font></p>
</body>
</html>

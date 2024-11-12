<!DOCTYPE html><html lang="en">
<head> 
<title>$(identity) 
</title> 
<link rel="icon" type="image/x-icon" href="img/favicon.ico"> 
<meta charset="utf-8"> 
<meta http-equiv="X-UA-Compatible" content="IE=edge"> 
<meta name="viewport" content="width=device-width, user-scalable=no"> 
<meta http-equiv="pragma" content="no-cache"/> 
<meta http-equiv="expires" content="-1"/> 
<link href="css/bootstrap.min.css" rel="stylesheet"> 
<link href="css/bootstrap.css" rel="stylesheet"> 
<link href="css/style.css" rel="stylesheet">
</head>
<body> 
<nav class="navbar navbar-default example6 navbar-fixed-top"> <div class="container"> 
<div class="navbar-header"> 
<button type="button" class="navbar-toggle collapsed tombol-nav" data-toggle="collapse" data-target="#navbar6"> 
<span class="sr-only">Toggle navigation</span> 
<span class="icon-bar"></span> 
<span class="icon-bar"></span> 
<span class="icon-bar"></span> 
</button> 
<a class="navbar-brand text-hide" href="login.html">Brand Text </a> 
</div><div id="navbar6" class="navbar-collapse collapse"> 
<ul class="nav navbar-nav navbar-right "> 
<li>
<a href="login.html" class="link-aktif">Home</a>
</li>$(if logged-in=='yes') 
<li class="dropdown"> 
<a class="dropdown-toggle dodown" class="tanpa-link" data-toggle="dropdown" href="#">Status 
<span class="caret"></span>
</a> 
<ul class="dropdown-menu"> 
<li>
<a href="status.html">Cek Masa Aktif</a>
</li>
<li>
<a href="logout.html">Logout</a>
</li>
</ul> 
</li>$(endif) 
</ul> 
</div>
</div>
</nav> 
<div class="container"> 
<div class="col-md-4 col-md-offset-4 col-sm-6 col-sm-offset-3 box-utama" style="padding:15px;">
<p style="font-size:28px; font-weight:700; text-align:center; color:#fff; margin-bottom: -5px;">LOGIN HOTSPOT</p>$(if error) 
<div style="color:#DF1A23; font-weight:bold; margin-bottom:5px;" class="kecil"> 
<script type="text/javascript">var error="$(error)"; var error1="user $(username) has reached uptime limit"; var error2="invalid password"; var error3="no valid profile found"; var error4="user &lt;$(username)&gt; not found"; var error5="no more sessions are allowed for user $(username)"; var error6="session limit reached ($(error-orig))"; var error7="web browser did not send challenge response (try again, enable JavaScript)"; var error8="invalid username or password"; var error9="user $(username) is not allowed to log in from this MAC address"; var error10="simultaneous session limit reached"; var error11="user $(username) has reached traffic limit"; var error12="uptime limit reached"; var error13="invalid Calling-Station-Id"; if (error==error1){window.location.href="expired.html";}else if (error==error2){window.location.href="exinvalid.html";}else if (error==error3){window.location.href="exnotfound.html";}else if (error==error4){window.location.href="exnotfound.html";}else if (error==error5){window.location.href="exterpakai.html";}else if (error==error6){window.location.href="exterpakai.html";}else if (error==error7){window.location.href="exbrowser.html";}else if (error==error8){window.location.href="exinvalid.html";}else if (error==error9){window.location.href="exmac.html";}else if (error==error10){window.location.href="exterpakai.html";}else if (error==error11){window.location.href="exkuota.html";}else if (error==error12){window.location.href="expired.html";}else if (error==error13){window.location.href="excalling.html";}else{document.write("$(error)");}</script> 
</div>$(endif) 
<form name="login" action="$(link-login-only)" method="post" $(if chap-id) onSubmit="return doLogin()" $(endif)> 
<input type="hidden" name="dst" value="$(link-orig)"/> 
<input type="hidden" name="popup" value="true"/>
<div style="padding:15px;"> 
<div class="form-group"> 
<div class="cols-sm-10"> 
<div class="input-group"> 
<span class="input-group-addon">
<span class="glyphicon glyphicon-user">
</span>
</span> 
<input type="text" class="form-control" name="username" placeholder="USERNAME" value="$(username)" required="required" autocomplete="off"/> 
</div>
</div>
</div>
<div class="form-group"> 
<div class="cols-sm-10" style="margin-top:-8px;"> 
<div class="input-group"> 
<span class="input-group-addon">
<span class="glyphicon glyphicon-lock">
</span>
</span> 
<input type="password" class="form-control" name="password" placeholder="PASSWORD" required="required" autocomplete="off"/> 
</div>
</div>
</div>
<div class="sedang"> 
<font color="#EDEDED"> Perhatikan penulisan <b>huruf besar dan kecil</b>
</font> 
</div>
<p style="margin-top:8px;"></p>
<center> 
<button onclick="window.location='https://laksa19.github.io/myqr';">QR</button> 
<button type="submit" class="btn btn-lg tombol-49 merah">
<span class="glyphicon glyphicon-log-in">
</span>&nbsp; LOGIN
</button>
</center> 
</div>
</form> 
<center> 
<img src="img/bw.png" class="img-responsive"> 
</center> 
</div>
</div>
<script src="js/jquery.js">
</script> 
<script src="js/bootstrap.min.js">
</script> <script src="js/modal.js">
</script> $(if chap-id) 
<form name="sendin" action="$(link-login-only)" method="post"> 
<input type="hidden" name="username"/> 
<input type="hidden" name="password"/> 
<input type="hidden" name="dst" value="$(link-orig)"/> 
<input type="hidden" name="popup" value="true"/> 
</form> 
<script type="text/javascript" src="md5.js">
</script> 
<script type="text/javascript">function doLogin(){document.sendin.username.value=document.login.username.value; document.sendin.password.value=hexMD5('$(chap-id)' + document.login.password.value + '$(chap-challenge)'); document.sendin.submit(); return false;}
</script> $(endif) 
<style>.blink{animation: blink-animation 1s steps(5, start) infinite; -webkit-animation: blink-animation 1s steps(5, start) infinite;}@keyframes blink-animation{to{visibility: hidden;}}@-webkit-keyframes blink-animation{to{visibility: hidden;}}
</style>
</body>
</html>

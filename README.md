<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Work From Home</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  font-family: Arial, sans-serif;
  background:#0f172a;
  color:white;
}

.banner{
  background:#020617;
  padding:15px;
  text-align:center;
  border-bottom:1px solid #1e293b;
}
.banner h1{
  margin:0;
  font-size:22px;
  color:#38bdf8;
}
.banner p{
  margin:5px 0 0;
  font-size:14px;
  color:#94a3b8;
}

.box{
  max-width:400px;
  margin:60px auto;
  padding:25px;
  background:#111827;
  border-radius:15px;
}

.box h2{
  text-align:center;
  color:#38bdf8;
}

input{
  width:100%;
  padding:12px;
  margin:10px 0;
  border:none;
  border-radius:8px;
  font-size:15px;
}

button{
  width:100%;
  padding:12px;
  margin-top:15px;
  background:#22c55e;
  color:black;
  border:none;
  border-radius:25px;
  font-size:16px;
  font-weight:bold;
  cursor:pointer;
}
</style>
</head>

<body>

<div class="banner">
  <h1>Work From Home</h1>
  <p>By Darpan.quant</p>
</div>

<div class="box">
  <h2>Register</h2>

  <input type="text" id="n" placeholder="Name">
  <input type="email" id="e" placeholder="Email">
  <input type="tel" id="p" placeholder="Number">
  <input type="text" id="s" placeholder="State">

  <button onclick="send()">Send</button>
</div>

<script>
function send(){
  var n = document.getElementById("n").value;
  var e = document.getElementById("e").value;
  var p = document.getElementById("p").value;
  var s = document.getElementById("s").value;

  if(n=="" || e=="" || p=="" || s==""){
    alert("Fill all details");
    return;
  }

  var text =
    "WFH Registration\n\n" +
    "Name: " + n + "\n" +
    "Email: " + e + "\n" +
    "Number: " + p + "\n" +
    "State: " + s;

  var url = "https://wa.me/9332307996?text=" + encodeURIComponent(text);
  window.open(url,"_blank");
}
</script>

</body>
</html>

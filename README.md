<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Join Our Website</title>

<script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>

<script>
(function(){
emailjs.init("0lXSpk6E_Y9ySmxZo");
})();

function sendMail(){

let gmail = document.getElementById("gmail").value;
let keyname = document.getElementById("keyname").value;

if(gmail=="" || keyname==""){
alert("Please fill all fields");
return;
}

emailjs.send("service_aodkhis","template_tt4bk37",{
gmail:gmail,
keyname:keyname
})

.then(function(response){

alert("Submitted successfully!");

}, function(error){

alert("Failed to send");

});

}
</script>

<style>

body{
font-family:Arial;
background:linear-gradient(135deg,#4facfe,#00f2fe);
height:100vh;
display:flex;
justify-content:center;
align-items:center;
}

.card{
background:white;
padding:40px;
border-radius:15px;
box-shadow:0 10px 30px rgba(0,0,0,0.2);
text-align:center;
width:320px;
}

input{
width:100%;
padding:12px;
margin-top:15px;
border-radius:8px;
border:1px solid #ccc;
}

button{
width:100%;
padding:12px;
margin-top:20px;
border:none;
background:#4facfe;
color:white;
border-radius:8px;
cursor:pointer;
}

</style>

</head>

<body>

<div class="card">

<h2>Join Us</h2>

<input type="email" id="gmail" placeholder="Enter your Gmail">

<input type="text" id="keyname" placeholder="Enter your Keyname">

<button onclick="sendMail()">Submit</button>

</div>

</body>

</html>

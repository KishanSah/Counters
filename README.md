# Counters
<!DOCTYPE html>
<html>
<head>
<title>Counter</title>
<link rel="stylesheet"
href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
integrity="sha384-
JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z"
crossorigin="anonymous">
<script
src="https://code.jquery.com/jquery-3.5.1.js"
integrity="sha256-QWo7LDvxbWT2tbbQ97B53yJnYU3WhH/C8ycbRAkjPDc="
crossorigin="anonymous"></script>
<script src="myscript.js"></script>
<script>
$(document).ready(()=>{
var a=0;
$("#incre").click(()=>{
if(a<10){
a=a+1;
colorchange(a);
$("#decre").prop('disabled', false);
}else{
$("#incre").prop('disabled', true);
}
$("#count").text(a)
})
$("#decre").click(()=>{
if(a>0){
a=a-1;
colorchange(a);
$("#incre").prop('disabled', false);
}else{
$("#decre").prop('disabled', true);
}
$("#count").text(a)
})
$("#reset").click(()=>{
a=0;
colorchange(a);
$("#count").text(a)
$("#incre").prop('disabled', false);
$("#decre").prop('disabled', false);
})
})
</script>
<script>
function colorchange(b){
if(b%2!=0){
$("#mydiv").removeClass("bg-primary");
$("#mydiv").addClass("bg-dark");
$("#headings").removeClass("text-dark");
$("#headings").addClass("text-light");
$("#count").addClass("text-danger");
$("#reset").addClass("btn-outline-light")
}
else{
$("#mydiv").removeClass("bg-dark");
$("#mydiv").addClass("bg-primary");
$("#headings").removeClass("text-light");
$("#headings").addClass("text-dark");
$("#count").removeClass("text-danger");
$("#reset").removeClass("btn-outline-light")
}
}
</script>
</head>
<body>
<div id="mydiv" class="container-fluid text-center text-white bg-primary py-5 mt-5">
<h1 id="headings" class="display-1 text-dark">Counter</h1>
<h1 id="count" class="display-1">0</h1>
<button id="decre" class="btn btn-danger">-</button>
<button id="reset" class="btn btn-dark px-3 mx-2">Reset</button>
<button id="incre" class="btn btn-success">+</button>
</div>
</body>


</html>

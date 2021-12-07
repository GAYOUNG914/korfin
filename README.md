# Korfin (한국핀테크산업협회)
Zeplin 으로 디자인을 받아 퍼블리싱 작업을 한 페이지입니다.
gnb, go to top 버튼, footer의 select box 등의 엘리먼트에 인터랙션을 구현해보았습니다.

## Link
* subpages
  - https://gayoung914.github.io/korfin/
  - https://gayoung914.github.io/korfin/index_member.html


## Tool
* HTML5
* CSS3
* SCSS
* Jquery

## Skill
* GNB의 Interaction<br><br>
👉 .nav > li에 호버를 하면 클래스가 붙으면서 GNB가 나타나고 언더바가 생성되어 호버 된 메뉴를 따라다니는 스크립트를 구현해보았습니다.
```
$(function () {
  //drop down & underbar event
  $(".nav > li").mouseover(function () {
    let leftValue = $(this).offset().left - 10,
      listWidth = $(this).width() + 20;
    $(this).addClass("on");
    $(this).find(".sub_gnb").addClass("on");
    $(".header_bg").addClass("on");
    $(".under_bar").addClass("on");
    $(".under_bar").css({ left: leftValue, width: listWidth });
  });
  $(".header_bg").mouseout(function () {
    $(".nav > li").removeClass("on");
    $(".nav > li > .sub_gnb").removeClass("on");
    $(".header_bg").removeClass("on");
    $(".under_bar").removeClass("on");
  });
  $(".nav > li > .sub_gnb").mouseout(function () {
    $(".nav > li").removeClass("on");
    $(".nav > li > .sub_gnb").removeClass("on");
    $(".header_bg").removeClass("on");
    $(".under_bar").removeClass("on");
  });
```

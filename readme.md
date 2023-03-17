# CSS 선택자 < 순서대로 해야 잘만들어짐 >
<style>
 {
    border:1px soild black;
    border-left:2px dashed red;
    border-style:double;
    border-left-color:green;
}

</style>
### css 박스 크기 계산 방법
<style>
box-sizing : content-box | padding-box | border-box

</style>

## 배치 속성
### 위치 속성
position : static | relative | absolute | fixed
- static : 정적, 기본값으로 별도의 position 속성을 지정하지 않아도 static으로 됨
- relative : 상대적인 위치로 설정시에 필요하며, 위치 좌표를 부모 기준으로 정할 경우 활용
- absolute : 절대적인 위치로 설정시에 필요하며, x좌표 위치와 y좌표 위치를 지정해야 함
    위치값은 auto 또는 px단위와 %단위 등으로 지정함
    left : 왼쪽 기준으로 부터의 위치
    right : 오른쪽 기준으로 부터의 위치
    top : 위쪽 기준으로 부터의 위치
    bottom : 아래쪽 기준으로 부터의 위치
    ※ x좌표 위치는 left나 right 중에서 하나만 기술하고, y좌표 위치는 top이나 bottom 중에서 하나만 기술해야한다.
- fixed : 화면에 고정된 위치를 설정할 때 필요하며, 스크롤시 fixed된 요소는 스크롤 되지 않고, 화면에 고정되어 있음.
    absolute과 마찬가지로 left/right, top/bottom의 위치를 설정해야 함.
- static이나 relative일 경우는 margin으로 떨어진 거리를 지정하고, absolute이나 fixed일 경우는 left/right, top/bottom으로 위치를 설정

### 레이어 속성
z-index : position이 absolute이거나 fixed일 경우 여러 콘텐츠 박스를 겹칠 경우 어떤 콘텐츠 박스를 앞에 배치할지 층(레이어)를 설정하는 것으로 숫자 정수만으로 지정하며, 
            숫자 값이 큰 것이 위(앞)에 배치됨.


### 흐름 속성
float : left | right | none
- position이 static이거나 relative일 경우 활용하는 배치 흐름 속성

### 흐름 해제 속성
clear : left | right | both | none
-float 설정된 박스의 흐름을 해제시 사용하며, float이 left로 설정되면, clear도 left로 하면 흐름이 해제되며, left나 right 모두 해제시에는 both를 사용하여 흐름을 해제함.

## CSS의 가시 속성
display : inline | block | inline-block | none
- 모든 태그 요소는 inline 또는 block 이거나 inline-block 요소이다.
- inline : 위/아래 마진이나 패딩 설정이 불가능하고, img나 video 등을 제외한 input, a, span, strong, em 등은 크기 지정이 불가능한 인라인 요소이다.
만약, 블록요소를 인라인 요소로 변경시에 활용
- block : h, p, ul, ol, dl, li, dt, dd, div, section,.. 등은 대부분 크기지정이 가능한 블록요소이다.
    만약, 인라인요소를 블록요소로 변경 시에 활용
- inline-block : 한 줄 안에 배치도 가능하고, 위/아래 마진/패딩 적용 가능, 크기 지정한 가시 속성
- none : 출력을 하지 않을 경우 활용

### 불투명도 속성
opacity : 0~1의 정수 또는 실수를 사용하여 지정(0:투명, 1:불투명)

### 가시 속성
visibility : visible | hidden
- visible : 보이기
- hidden : 숨기기
- display : none과 달리 hidden을 하면, 안보이는 것 뿐이지 그 자리를 차지하고 있음.

## 넘침 속성
overflow : hidden | scroll | auto | visible
hidden : 흘러 넘치는 부분을 숨김
scroll : 흘러 넘치든 안 넘치든 무조건 스크롤바로 표시
auto : 흘러 넘칠 경우만 스크롤바 표시
visible : 기본값으로 흘러 넘쳐도 그냥 콘텐츠를 모두 표시
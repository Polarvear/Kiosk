# Kiosk
버전 관리 하는 법 찾아보는중
+-버튼 클릭시 숫자늘어나는 기능 완료
개선할 사항 : -버튼 클릭 시 0미만으로 출력하면 안됨
개선완료
개선할 사항 : 가격을 출력해주는 기능을 만들어야하는데 최종적인 Qty값을 못 받아오고 있음
최종 qty들고오는 것에는 성공했짐나 price데이터를 받아오지 못하고 있음 이해 안되는 부분에 대해서 더 공부할 예정
line250, 251

구조분해 할당으로 orders에 push 하는 것에는 성공했지만 console.log(orders) 와 console('orders는'+orders)로 출력했을 때 첫 번째는 객체리터럴을 성공적으로 반환하는 반면 두 번째 출력은 [object Object]라고 반환하는데 이것이 무엇인지 궁금함 prototype과 prototype chain에 대해서 기본 지식을 지니고 있어야함
허접하지만 화면에 출력완료 개선할 사항으로는 현재 버튼 클릭시 숫자가 초기화가 되지 않음. 총 주문 금액이 출력이 안되고 있음.
처음 개선할 것으로는 클릭시 숫자 초기화 기능 넣기 이후 총 주문금액 넣어주기

버튼 클릭시 숫자 초기화 완료.
총 주문금액 출력해보기 완료.

이후 개선사항 같은 물품 클릭시 기존의 물품에 추가해주기
    주문한 물품 취소기능 넣어주기

    삭제기능은 추가해줬는데 지금 문제는 버튼 클릭하고 li태그가 사라지는데 다시 주문을 하게되면 버튼 클릭 이전의 주문 목록들이 생기는 문제발생 그래서 새로생성되는 delBtn만을 컨트롤 해보려고 함

 delBtn만을 컨트롤을 완료 그러나 이전에 잘 동작하던 코드들이 꼬이는 문제가 발생, delBtn을 클릭 두번해야 삭제 기능 발생, 삭제를 하게 되면 sum값이 동작하지 않음. ADD Cart버튼 클릭시 이전에 존재하던 로그도 불러오는 문제 발생 이전에 작성했던 li를 클릭해도 되던 전의 코드를 참조해야할 듯

 이전 버전을 들고왔는데도 똑같은 문제발생 계속 물고있는 애가 누구인지 찍어보는 게 필요할 듯
 splice 기능을 사용하면 좋을 듯 그러기 위해서는 button에 data-idx값을 줘보자 qty값도 초기화가 안됨 즉 처음 모달창이 생성되었을 때는 1이라고 나와있지만 +버튼 클릭시 증가가 갑자기 6에서부터 증가한다든가의 문제발생

 qty값 해결완료, showOrderItem 함수 정의해서 코드를 간결하게 만들었음 splice 기능을 사용하면 될 것 같은데 현재 뭔가 기능이 꼬인 것 같은데 정확하게 뭐가 꼬인 건지 모르겠음 ADD Cart 버튼 클릭시 예전에 있던 애들도 불러오고 있음 정확하게 찍어봐야 할 듯

line 249번째에서 push해줄 때 기능에 문제가 생긴 것 같음. push 문제는 브라우저 문제였던 것 같음 현재는 제대로 동작중..아니면 어제 착각했을 가능성도 있음. 새롭게 개선할 사항은 예를 들어 빅맥을 showOrderItem에 추가해줬을 때 추가로 빅맥을 주문하는 경우 기존의 orders에 들어가도록 손 봐야겠음. 그리고 sum값이 앞의 품목부터 삭제했을 때 제대로 동작하지 않는 문제도 손 볼 것


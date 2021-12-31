# 트러스트를 해봅시다

## 해보기 전에
플러그인이 있으면 좋습니다 → Triggernometry.dll 

이 플러그인은 Release에서 받은 ACT Set에 당연히 들어있기에 따로 안찾아도 됩니다.

## 매크로를 준비합니다
매크로는 중간 쫄 잡을 때 쓰면 좋습니다. 위의 플러그인도 이 매크로를 반복해서 사용할 수 있게하려고 쓰는 검미.

흥마 기준으로 해볼까요

![image](https://user-images.githubusercontent.com/7216647/147810844-ef6082f7-4ae7-483c-a898-ee63d2f14c21.png)

복사용은 다음과 같습니다
 ~~~
/ac Swiftcast <wait.1>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Blizzard II <wait.3>
/ac Thunder II <wait.3>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Fire II <wait.3>
/ac Blizzard II <wait.3>
/ac Thunder II <wait.3>
/e ATTACK END!!!! <se.2>
~~~

## 해봅시다
그냥 쫄한테 저 매크로를 쓰면됩니다. echo로 "ATTACK END!!!!" 메시지와 se 이펙트 삑 소리가 나면 다시 매크로를 입력하면 됩니다. 참 쉽죠....는 이것도 귀찮슴다!!! 그냥 이것 마저도 귀찮져! 여기서 triggernometry가 등장합니다!

## Triggernometry 설정
![image](https://user-images.githubusercontent.com/7216647/147810864-641d96e0-c39c-4eba-9f83-21e721404387.png)

복사용 ML은
~~~
<?xml version="1.0"?>
<TriggernometryExport Version="1">
  <ExportedTrigger Enabled="true" Name="트러스트용" Id="c2c463ea-c93b-48eb-9727-d7f8f86a4fa5" RegularExpression="ATTACK END!!!!" Description="공격이 끝나면 또 공격">
    <Actions>
      <Action OrderNumber="1" KeypressType="WindowMessage" KeyPressCode="112" KeyPressWindow="FINAL FANTASY XIV" TextAuraFontSize="8.25" TextAuraFontName="Microsoft Sans Serif" ActionType="KeyPress" ExecutionDelayExpression="2000">
        <Condition Enabled="false" Grouping="Or" />
      </Action>
    </Actions>
    <Condition Enabled="false" Grouping="Or" />
  </ExportedTrigger>
</TriggernometryExport>
~~~

이 복사용 ml을 xml 파일로 저장하고, Triggernometry에서 Import를 하면 편하겠죠.

![image](https://user-images.githubusercontent.com/7216647/147810892-647c4e5d-c401-452f-9b7b-32ad6a9b8690.png)

이 Triggernometry 항목을 체크 해둡니다. 

그리고 F1입력에 해당하는 곳에 위에서 만든 매크로를 갖다 둡니다

![image](https://user-images.githubusercontent.com/7216647/147810914-103b5019-0d7a-445f-bdaa-9df6576fbd4f.png)

스샷에는 CTRL+1로 나오는데, F1위치 입니다. 컨트롤러 사용자라 키보드의 세계는 잘 모르겠슴미다....

암튼, 그렇슴다 끝입니다. 이 Triggernometry가 하는 일은 매크로가 끝날때 나오는 "ATTACK END!!!!" 메시지가 확인되면 1초 후에 F1키를 눌러주는 역할을 하는 것이었던 것임미!

## 보스는?
그냥 잡으세요... 그냥 잡는게 속편합니다. 이걸로 해도 되긴하는데, 어짜피 무빙은 해야하고 매크로만 누르고 안보고 있다가 장판에 깔려 누은 내 모습을 발견...하기 전에 스타트 리셋 지점에 서 있는 모습이 보일검미

게다가 우리 scion 동료들은... 약해욧.


## 탱크랑 힐러도 되능가!
해보니깐 힐러도 됩니다. 우리 산크레드만 힐해주면 되긴합니다

![image](https://user-images.githubusercontent.com/7216647/147810958-b25782a8-b8a8-4ff5-8ff0-2214b5b5dab5.png)

**탱크는 안됩니다...** 알피노랑, 우리엔게가 커버를 못해요...

참고로, 바드랑 총잡이는... 정말 편합니다. 바드 매크로를 한번 볼까요

![image](https://user-images.githubusercontent.com/7216647/147811010-3d97aaa8-200e-42b1-a043-1071517a76a2.png)

Quick Nock만 쓰면 됩니다. 중간에 Rain of Death나 노래도 좀 넣어주면 좋긴하겠지만, 그냥 Quick Nock 하나면 끝입니다. 비슷하게 총잡이는 Spread Shot만 넣으면 됩니다. 다른 기술 넣어도 되는데, 어짜피 트러스트는 빨리하나 늦게하나 30분입니다...

*하지만 애들만 싸우게 냅두면 45분 이상은 각오해야하겠죠*

## HUD 배치
![image](https://user-images.githubusercontent.com/7216647/147811111-35142c58-20c6-4d17-9c38-a8a0603a5770.png)

시작하기 위한 매크로, 풀링용 scathe 랑, 타겟을 바꾸기 위한 Target Next를 배치합니다. 왼쪽 아래 Return 모양 매크로는 Triggernometry의 연속 사용을 막기 위해 쫄 구간이 끝나면 입력하는 아무 내용없는 매크로 입니다.

![image](https://user-images.githubusercontent.com/7216647/147811118-447d7884-4dc7-467f-ad0d-47f28c5f6e52.png)

FATE 돌아댕기기 할때도 쓰려고 레벨 싱크를 넣어놓긴 해쓰요.

이게 왜 필요하냐하면, Triggernometry는 매크로에서 출력하는 "ATTACK END"를 캐치하고 계속 키를 눌러주는데, FF14는 매크로 실행중에 다른 매크로를 실행하면 실행하던 매크로를 캔슬시키므로, 저 "ATTACK END"메시지를 출력 안하게 하는 방법으로 이 캔슬 기능을 사용하는것이겠지요

한편 폴리가 남으면 쓸 Foul과 쫄을 잡았을때 Fire상태면 MP수급이 애매하니깐 Transpose도 넣어 뒀습니다


## 다른 JOB
사실 이 방법은 레인지 계열이 최고 편합니다. 무빙되지, 캐스팅 없지, 거리 멀지. 그렇다고 밀리가 안되는것도 아닙니다. 쫄 장판 맞아도 알피노와 우리엔게는 그정도는 힐해주거든여


## 끝
이걸로 편하게 트러스트를 해보아욧!
5.0 때는 Triggernometry안쓰고 책보면서 매크로 눌렀는데, 6.0에는 Triggernometry를 도입했더니 패드에서 손떼고 일을 할 수 있어(?) 편했습니다. 대충 쫄 구간 2분 정도 예상하면 되니깐 매크로 눌러놓고 딴짓하다 2분후 쯤 보고 이동하면 됩니다.


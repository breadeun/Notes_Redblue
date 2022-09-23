Android Studio 프로젝트, 패키지명 변경
-

**1. 디렉토리명 변경**

프로젝트 네비게이션 바에서 설정버튼을 누르면 **Compat Middle Package** 메뉴가 보입니다.
현재는 선택 상태로 패키지명을 기준으로 폴더가 구조화 되어 있습니다. 이를 해제 시켜줍니다.

![](attachments/Pasted%20image%2020220922152618.png)

디렉토리가 해제되면 아래와 같이 폴더 이름을 변경할 수 있습니다.
저는 example과 timertutorial 이 두 곳을 수정했습니다.

![](attachments/Pasted%20image%2020220922152901.png)

Rename선택시 Warining이 나타나도 Rename Package 선택하여 변경될 수 있게 해줍니다.
이때 하단 창에 변경되는 내역이 표시되는데, **Do Refactor**를 클릭하여 변경을 해줍니다.
저는 아래와 같이 디렉토리 명이 변경되었습니다.

![](attachments/Pasted%20image%2020220922152913.png)

**2. build.gradle 파일 변경**

build.gradle app 파일에 들어가 **applicationId**를 변경해 줍니다.

![](attachments/Pasted%20image%2020220922152959.png)

**3. Rebuild Project**

프로젝트를 rebuild를 해줍니다. 이때 import 부분에서 문제가 생길 수 있으나 다시 import 해주면 됩니다.

**4.  res > values > string.xml → app_name, app_code_name, app_pakcage_name 변경**

app_package_name 변경시에는 admin_code 테이블 확인

![](attachments/스크린샷%202022-09-22%20오후%204.03.19.png)

** 5. res > drawable-xhdpi 에 스플래시 x3 png 추가 **

![](attachments/스크린샷%202022-09-22%20오후%203.39.58.png)

**6. activity_spalsh.xml 파일 수정**

![](attachments/스크린샷%202022-09-22%20오후%203.40.54.png)

**7. settings.gradle → rootProject.name 변경 **

![](attachments/스크린샷%202022-09-22%20오후%203.43.16.png)

8. 512 앱 아이콘 png main 에 복사

![](attachments/스크린샷%202022-09-22%20오후%203.45.56.png)

9. res > 우클릭 > new > image Asset > Lancher Icon 추가

아이콘이 꽉 찰 정도로 scaling 조정

![](attachments/스크린샷%202022-09-22%20오후%203.47.58.png)


10. AndroidManifest.xml icon 변경 

![](attachments/스크린샷%202022-09-22%20오후%203.51.44.png)

11. FirebaseMessagingService.java 아이콘 변경

![](attachments/스크린샷%202022-09-22%20오후%203.53.08.png)

12. app > google-services.json 파일 변경
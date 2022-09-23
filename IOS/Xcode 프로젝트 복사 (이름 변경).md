Xcode 프로젝트 복사 (이름 변경)
-

**1. 프로젝트로 간다.**

**2. 왼쪽 Project Navigator로 간다.**

![](attachments/Pasted%20image%2020220921121427.png)

**3. 맨 위의 프로젝트 파일을 클릭하고, 엔터를 쳐준다.**

![](attachments/Pasted%20image%2020220921121452.png)

그럼 이렇게 이름을 바꿀 수 있게 됩니다.
이름을 원하시는 이름으로 바꿔주세요. 저는 RenameTest라고 해볼게요 :)
그리고 엔터를 딱 치면

![](attachments/Pasted%20image%2020220921121503.png)

이런 화면이 나오는데, Rename을 눌러주세요 :)  
이러면 이제 빌드가 되야 할 것 같지만 안됩니다.

**4. Product -> Scheme -> Manage Scheme에 간다.**

![](attachments/Pasted%20image%2020220921122317.png)

네 저기에 들어가주세요 :)
그러면

![](attachments/Pasted%20image%2020220921122328.png)

이러한 화면이 나오게 됩니다. 
왼쪽 Scheme에는 우리의 예전 프로젝트 이름이 들어가 있네요. 이거 바꿔줍시다.
저 옛날 프로젝트 이름부분을 클릭하고 엔터를 쳐주세요. 
**더블클릭 X!!!!!더블클릭 하면 안됩니다.**
**엔터만 쳐주세요.**

![](attachments/Pasted%20image%2020220921122357.png)

이렇게 편집이 가능해 집니다. 우리의 새로운 프로젝트 이름을 넣어주세요. 
넣고, 엔터를 쳐주시면 된답니다.

![](attachments/Pasted%20image%2020220921122405.png)

close해주세요.
그러면 드디어!!!!!!!!...될 것 같지만, 안되네요.

**5. Xcode를 종료한다.**

네. 종료해주세요 :)

**6. 내 프로젝트 폴더를 본다.** 

![](attachments/Pasted%20image%2020220921122255.png)

네! 얘는 아직 Coretext네요 :)
**이 폴더 이름을 바꿉시다.**
그리고 폴더를 열어주시면

![](attachments/Pasted%20image%2020220921122242.png)

쟤도 아직 Coretext네요. 저 폴더도 바꿔줍시다.  

**7. 프로젝트를 연다.**

그러면..

![](attachments/Pasted%20image%2020220921122421.png)

ㅇ..?

![](attachments/Pasted%20image%2020220921122428.png)

  
네..이런 오류들을 볼 수 있ㄴ는데 괜찮아요..!!
거의 다 했어요.

**8. 왼쪽 Project Navigator의 폴더를 클릭한다.**

![](attachments/Pasted%20image%2020220921122435.png)

네 이번엔 제일 위에 있는 프로젝트말고!!!!!**저 폴더를 클릭해줍니다.**

**9. 그 상태에서 오른쪽 File inspector를 본다.** 

![](attachments/Pasted%20image%2020220921122442.png)

그럼 저렇게 location밑에 폴더 모양을 볼 수 있어요.   
그걸 눌러줍니다. 

![](attachments/Pasted%20image%2020220921122449.png)

가장 바깥쪽의 폴더 말고 저 코드를 가지고 있는 안쪽 폴더를 지정하고 Choose를 눌러주세요.

![](attachments/Pasted%20image%2020220921122501.png)

그럼 여전히 얘네가 빨간색으로 표시될텐데, **Xcode를 종료하시고 다시 들어오면** 

![](attachments/Pasted%20image%2020220921122506.png)

정상적으로 되어 있는 모습을 볼 수 있어요.
이제 빌드하면..

![](attachments/Pasted%20image%2020220921122521.png)

이런 에러를 볼 수 있습니다.
해결하러 가요!!

**11. 타겟 -> Build Settings -> info.plist 검색 -> info.plist File 변경**

![](attachments/Pasted%20image%2020220921122529.png)

네. 이렇게 찾아가주세요. 
info.plist File다들 찾으셨나요? 

![](attachments/Pasted%20image%2020220921122540.png)

이부분은 여전히 우리의 옛날 프로젝트 이름이네요. 바꿔줍시다. 
저 Coretext/Info.plist부분을 **더블클릭**해주세요. 

![](attachments/Pasted%20image%2020220921122547.png)

그리고 바꿔줍니다. **내 새로운 프로젝트 이름/Info.plist**

**12. Product Bundle Identifier를 바꾼다.**

방금 바꾼 Info.plist File 조금 밑에 보시면

![](attachments/Pasted%20image%2020220921122555.png)

Product Bundle Identifier라고 있는데, 이것도 바꿔줍시다. 

![](attachments/Pasted%20image%2020220921122610.png)

우리에게 익숙한 화면인

![](attachments/Pasted%20image%2020220921122605.png)

여기서 바꿔주셔도 상관없어요 :)
그럼 이제...!!

![](attachments/Pasted%20image%2020220921122616.png)

XD
프로젝트 이름 바꾸기가 이렇게 복잡하다니..
아무튼 도움이 되었으면 좋겠습니다 :)

**13. bodycodi members.entitlements → #{projectName}.entitlements**

![](attachments/스크린샷%202022-09-21%20오후%203.44.34.png)

Targets → Build Settings → Code Signing Entitlements 이름 변경

**14. Pods, Podfile.lock, bodycodi members.xcworkspace 삭제, Podfile 변경, pod deintegrate, podInstall**
- target '#{projectName}' do

출처: [https://zeddios.tistory.com/286](https://zeddios.tistory.com/286) [ZeddiOS:티스토리]
Xcode 프로젝트 Display Name 띄어쓰기
-

**1. Info.plist를 Source Code로 열기**

Info.plist 우클릭 > Open As > Source Code 선택

![](attachments/Pasted%20image%2020220921155110.png)

**2. CFBundleName에 띄어쓰기 대신 &#x2007; 를 입력**

![](attachments/Pasted%20image%2020220921155142.png)


This is because of a change Apple made in iOS 11 for truncating for longer app names. If the name is longer than 12 characters, the spaces will be removed. Otherwise, they'll still exist.

For example, `Guide book app` will become `Guidebookapp`, but `Gui boo app` will stay as `Gui boo app`.

Using unicode `&#x2007;` ([FIGURE SPACE](http://www.fileformat.info/info/unicode/char/2007/index.htm)) works because it isn't an ascii space. I would be hesitant to use this as a solution because it seems reasonable that Apple would "fix" this bug and remove `&#x2007;` for apps with names longer than 12 characters.
- WINODWS

1. 윈도우 검색 -> Windows PowerShell 실행

2. wsl --install 입력

3. 설치 완료후 재부팅

4. 재부팅 후 터미널창이 뜨면 사용자 아이디 및 비밀번호 설정 후 설치 완료.

5. visual studio code 설치

6. "WSL" 확장 프로그램 설치 (+ 추가 C/C++ 확장 프로그램 설치는 자유)

7. 간단한 c 코드 작성 및 컴파일 확인

   - 컴파일러는 gcc/g++ 사용, 터미널 창에서 빌드 및 실행을 할 예정
   
***Ubuntu 설치 오류시
1.  C:\Users\IT대학_000>wsl --install -d Ubuntu
Ubuntu이(가) 이미 설치되어 있습니다.
Ubuntu을(를) 시작하는 중...
디스크 'C:\Users\IT대학_000\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu_79rhkp1fndgsc\LocalState\ext4.vhdx' WSL2에 연결하지 못했습니다. 지정된  파일을 찾을 수 없습니다.
Error code: Wsl/Service/CreateInstance/MountVhd/ERROR_FILE_NOT_FOUND
디스크 'C:\Users\IT대학_000\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu_79rhkp1fndgsc\LocalState\ext4.vhdx' WSL2에 연결하지 못했습니다. 지정된  파일을 찾을 수 없습니다.
Error code: Wsl/Service/CreateInstance/MountVhd/ERROR_FILE_NOT_FOUND
디스크 'C:\Users\IT대학_000\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu_79rhkp1fndgsc\LocalState\ext4.vhdx' WSL2에 연결하지 못했습니다. 지정된  파일을 찾을 수 없습니다.
Error code: Wsl/Service/CreateInstance/MountVhd/ERROR_FILE_NOT_FOUND
Press any key to continue...
--> wsl --unregister Ubuntu

또는 wsl --unregister Ubuntu-22.04
이후 wsl --install 다시 진행
2. wsl --update 이후 wsl --install 다시 진행

-------- 03. 16. 추가 ----------

재설치 시 다음 순서로 진행
1. 설정 - 앱 - 앱 및 기능이동
2. Linux 검색 -> linux용 하위 시스템 ~~~ 제거
3. Ubuntu 검색 -> 제거
4. 재부팅
5. 이전 공지 wsl --install 부터 다시 진행





1. visual studio code 실행

- 왼쪽 아래에 wsl:ubuntu 라고 적혀있는 경우 이미 연결된 상태의 창을 보고 있으므로 "4-1 참조"

!(https://canvas.knu.ac.kr/courses/20364/files/1196320/preview)

2. 왼쪽 목록에서 "Extensions" 클릭 후 wsl 검색, Microsoft가 배포하는 확장팩 설치

[스크린샷 2023-03-16 오후 2.39.03.png](https://canvas.knu.ac.kr/courses/20364/files/1196347/preview)

3. 설치 완료 후 왼쪽 목록에서 Remote Explorer 클릭, Ubuntu에 마우스 커서 올릴 때 표시되는 폴더 모양(Connect to WSL) 클릭

[스크린샷 2023-03-16 오후 2.40.40.png](https://canvas.knu.ac.kr/courses/20364/files/1196359/preview)

4. 새로운 창이 뜨고 기본 설정에 필요한 도구들이 다운된 후 왼쪽 아래에 WSL: Ubuntu가 표시되면 연결된 것.

[스크린샷 2023-03-16 오후 2.45.27.png  ](https://canvas.knu.ac.kr/courses/20364/files/1196376/preview)

4-1. 만약 연결을 해제하고 싶은 경우 WSL: Ubuntu 클릭, 중앙 상단에 목록에서 "Close Remote Connection" 클릭

[스크린샷 2023-03-16 오후 2.47.25.png](https://canvas.knu.ac.kr/courses/20364/files/1196383/preview)

 5. Ubuntu 폴더를 add on 하기 위해 왼쪽 목록에서 "Explorer" 선택 후 Open Folder 클릭, "/home/${설치때 본인 설정한 이름}/" 위치 확인후 OK.

권한 설정 창이 뜨면 Trust 해주면 된다.

[스크린샷 2023-03-16 오후 2.49.29.png](https://canvas.knu.ac.kr/courses/20364/files/1196405/preview)

6. 연결되면 왼쪽 창에 폴더 목록이 표시된다. 우클릭 후 "New File" 선택, main.c 파일 생성

[스크린샷 2023-03-16 오후 3.05.30.png](https://canvas.knu.ac.kr/courses/20364/files/1196486/preview)

7. main.c 코드 작성 후 저장 (Ctrl + S)

(저장이 안된 경우 중앙 상단 main.c 파일 이름 왼쪽에 동그라미 표시가 되어 있음)

[스크린샷 2023-03-16 오후 3.06.39.png](https://canvas.knu.ac.kr/courses/20364/files/1196500/preview)

8. 터미널창이 열려있지 않다면 왼쪽 상단 목록에서 Terminal -> New Terminal 클릭 (또는 Ctrl + Shift + ` )

[스크린샷 2023-03-16 오후 3.09.01.png ](https://canvas.knu.ac.kr/courses/20364/files/1196511/preview)

9. 터미널 창에서 다음 명령어를 차례대로 입력, 처음 한번 명령어 실행시 비밀번호를 입력해야 함. 본인 설치때 설정한 비밀번호 설정

$ sudo apt update

$ sudo apt install build-essential

-> 입력후 엔터 치면 설치됨

[스크린샷 2023-03-16 오후 3.11.56.png](https://canvas.knu.ac.kr/courses/20364/files/1196520/preview)

[스크린샷 2023-03-16 오후 3.13.12.png](https://canvas.knu.ac.kr/courses/20364/files/1196524/preview)

10. 설치 완료 후 터미널 창에서 gcc 입력시 다음과 같이 출력되면 설치 완료.

[스크린샷 2023-03-16 오후 3.14.33.png](https://canvas.knu.ac.kr/courses/20364/files/1196530/preview)

11. 다음 명령어들 순서대로 입력해서 코드 실행 확인

$ gcc main.c -o main

$ ./main

[스크린샷 2023-03-16 오후 3.15.38.png ](https://canvas.knu.ac.kr/courses/20364/files/1196537/preview)

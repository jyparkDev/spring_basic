> # 남궁성의 Spring framework 강좌 - 기본편
> Spring 입문자를 위한 최고의 강좌.  https://fastcampus.co.kr/                
> Spring framework 강좌 - 심화편(준비중)  
> Spring boot 강좌 - 기본편(준비중), 심화편(준비중)  
> email : seong.namkung@gmail.com    
<br>

# Part1. Spring 시작하기
## 1. 개요    
  - ### Spring이란?  
    Spring makes it easy to create Java **enterprise** applications.  
    https://spring.io/  
    https://docs.spring.io/spring-framework/docs/current/reference/html/overview.html#spring-introduction  
  - ### Spring MVC란?  
    A Spring MVC is a framework to build web applications. It follows the MVC(Model-View-Controller) design pattern.
    https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/mvc.html  
    <br>
    **[참고]** MVC패턴이란? https://developer.mozilla.org/ko/docs/Glossary/MVC  
<br>

## 2. 설치 & 설정  

1. git 설치 - https://git-scm.com/downloads   
  
    [Mac] 먼저 terminal열고, 아래와 같이 입력하고 엔터치세요.   

           $ git
           
     'git'명령어는... 도구를 설치하시겠습니까?라고 묻는 창이 열리면 '설치'를 클릭.(몇분 소요) 설치 완료 후, 아래와 같이 입력후 엔터.
           
           $ git --version  
           git version 2.28.0  

    위와 같이 나오면 설치가 잘된 것입니다. 버전이 조금 달라도 괜찮습니다.  
    <br>
2. SDKMAN을 이용한 JDK1.8 설치 - https://sdkman.io/install  
    ```
      $ curl -s "https://get.sdkman.io" | bash  
      $ source "$HOME/.sdkman/bin/sdkman-init.sh" 
    ```

   **[참고]** Windows에서 설치 중 not found zip에러 발생시, 
        https://sourceforge.net/projects/gnuwin32/files/zip/3.0/ 에서 zip-3.0-bin.zip,    
        https://sourceforge.net/projects/gnuwin32/files/bzip2/1.0.5/ 에서 bzip2-1.0.5-bin.zip을 다운로드  
        압축 해제 후, zip.exe와 bzip2.dll을 'git설치폴더\bin' 폴더(예:C:\Program Files\Git\bin)에 넣어줍니다.  
  
    $ sdk version  <--- sdkman 버전출력  
    $ sdk java list  <-- 설치 가능 & 설치된 JDK목록  
    $ sdk install Identifier <--- 지정된 JDK설치(Identifier대신 8.292.10.1-amzn와 같이 원하는 종류와 버전 지정)  
    $ sdk java current <--- 현재 사용중인 java버전 출력  
    $ sdk use java 버전 <--- 현재 사용중인 java버전을 지정된 버젼으로 변경  
    $ echo $JAVA_HOME <--- JAVA_HOME으로 지정된 경로 출력  
    $ sdk uninstall java 버전  <--- 지정된 버전의 자바를 uninstall  

  
    **[참고]** SDKMAN없이 JDK직접 설치할 때는 아래의 동영상을 참고하세요.  
            [\[YouTube\] 자바 개발도구 JDK 설치 방법](https://youtu.be/Q1AGokud_x4) - Windows 10   
            [\[YouTube\] 자바 개발도구 JDK 설치 방법](https://youtu.be/Q1AGokud_x4) - MacOS
<br>

3. Tomcat 9 설치 - https://tomcat.apache.org/download-90.cgi  
  [Windows] https://mirror.navercorp.com/apache/tomcat/tomcat-9/v9.0.50/bin/apache-tomcat-9.0.50-windows-x64.zip  
  [Mac] https://mirror.navercorp.com/apache/tomcat/tomcat-9/v9.0.50/bin/apache-tomcat-9.0.50.tar.gz  
        <br>
    다운로드 받은 파일을 설치하고자하는 디렉토리로 이동후 아래의 명령을 실행. 압축을 풀어서 사용자의 홈디렉토리(~)에 저장.  

    ```
        $ tar -xvf apache-tomcat-9.0.50.tar.gz -C ~  
    ```

   **[참고]** 버전별 비교    - https://tomcat.apache.org/whichversion.html  
  <br>
  
4. STS, IntelliJ 설치   
- **STS 3.9.17**  
**Windows** - https://download.springsource.com/release/STS/3.9.17.RELEASE/dist/e4.20/spring-tool-suite-3.9.17.RELEASE-e4.20.0-win32-x86_64.zip  
**MacOS** - https://download.springsource.com/release/STS/3.9.17.RELEASE/dist/e4.20/spring-tool-suite-3.9.17.RELEASE-e4.20.0-macosx-cocoa-x86_64.dmg  

- **IntelliJ**   
**Windows** - https://www.jetbrains.com/idea/download/#section=windows  
**MacOS** - https://www.jetbrains.com/idea/download/#section=mac  
<br>

5. VS Code 설치 - https://code.visualstudio.com/download  
  - 유용한 플러그인  
  한글 팩 - https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ko  
  open in browser - https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser  
  Prettier - Code formatter - https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode  
  indent-rainbow - https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow  


  
  


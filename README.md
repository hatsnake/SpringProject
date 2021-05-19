# SpringProject
SpringProject Default Settings

STS 스프링 기본세팅 프로젝트 가져오기

git bash
$ git init
$ git remote add origin https://github.com/hatsnake/SpringProject.git
$ git pull origin master
$ git remote remove origin

STS
- 스프링 프로젝트 가져오기
FILE -> Open Projects from File Systems... 에서 Servers, SpringProject를 각각 선택하고 Finish

- 톰캣서버 추가
Servers에서 tomcat서버를 만들고 Modules에서 Path를 /로 수정

- STS 인코딩 및 기본설정 가져오기
File -> import... -> Preferences에서 SpringProjectSettings.epf를 선택, 
import all 체크상태로 Finish

- 오라클,마이베티스 연결 확인
root-context.xml안에 username과 password를 본인 DB계정에 맞게 변경
src/test/java안에 있는 MybatisTest.java와 OracleConnectionTest.java
를 JUnit Test를 통해 DB연결이 됐는지 확인

$ git status
$ git add .
$ git commit -m "ADD import SpringProject"
$ git push origin master

결과 : STS에서 Oracle & Mybatis연결관련 설정, STS의 한글 인코딩 및 기본 세팅 등의
       프로젝트를 한번 만들때 마다 해줘야하는 설정을 가져와서 바로 프로젝트를 만들수 있음.
       다만 환경에 따라 다른 부분이 있기 때문에 기본적으로 세팅하는법을 이해한 후
       사용해야지 문제없이 적용할 수 있음.

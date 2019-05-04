# [참고] 직접 사용하기 위해 fork 후 수정한 부분
- 기능 수정
  - 테이블 명세서가 개별 시트에 만들어지는 부분을 하나의 시트에 만들어지도록 수정
    - 테이블이 256개 이상인 경우 시트 개수 제한으로 인해 실패하는 문제 있었음
    - 테이블이 많은 경우 시트를 이동하며 내용을 확인하는데 어려움이 있었음

- 사용법 및 설정파일 git에 추가
  - [output/README.md](output/README.md)
    
- 추가 고려사항
  - 하나의 시트에 모든 테이블 명세서가 있는 경우도 테이블이 너무 많으면 보기 어려움
     - 테이블 개수가 일정 기준 이상인 경우에만 시트 분리가 필요하지 않을까?
     - 보통 연관 있는 테이블들은 prefix 가 동일하므로 테이블명의 첫번째 알파벳으로 시트를 나누는 방법?
     - 스마트한 시트 분리가 되면 좋지만 테이블명 설계 방식에 따라 케바케이므로 일단 보류


# MySQL 테이블 명세서 생성 프로그램
이 프로그램은 itpaper가 진행하는 개발자과정 수강생들의 팀 프로젝트 활동에 도움이 되고자 작성되었습니다. 
MySQL의 테이블 구조를 조회하여 엑셀로 명세서를 저장해주는 프로그램 입니다. 프로그램 UI는 구성하지 않았습니다.

- 저작도구: Eclipse
- 사용언어: JAVA

사용시에는 config.xml 파일의 데이터베이스 접속 정보를 수정하여 사용하시기 바랍니다. 자세한 사용법은 다음의 URL을 참고하시면 됩니다.

[itpaper_link]: http://www.itpaper.co.kr/mysql-테이블-명세서-생성-프로그램

![Alt text](http://www.itpaper.co.kr/wp-content/uploads/2016/06/2b1561e56127e458e66568948d7ff24b.png)

## 사용된 라이브러리
- https://github.com/virtuald/curvesapi
- MySQL Connector java : https://dev.mysql.com/downloads/connector/j/3.0.html 
- MyBatis3 : http://www.mybatis.org/mybatis-3/ko/
- Apache Log4j2 : https://logging.apache.org/log4j/2.x/
- Apache POI Library : https://poi.apache.org/
- Apache XML Beans : https://xmlbeans.apache.org/

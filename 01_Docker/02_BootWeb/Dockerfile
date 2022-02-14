# 베이스 이미지
FROM openjdk:11
# 작성자 라벨 설정
LABEL maintainer "kh<kh@iei.com>"
# 버전 라벨 생성
LABEL version="1.0"
# 컨테이너에 /root 디렉터리에 빌드 컨텍스트 안에 있는 ~.jar 파일을 카피하겠다.
COPY 05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar /root
# 타임존 설정
ENV TZ=Asia/Seoul
# /root 디렉토리로 작업 디렉터리를 바꾼다. 프롬프트가 /root로 이동되면서 작업 디렉터리가 됨
WORKDIR /root
# 포트 노출
EXPOSE 8088
# 처음 실행할 명령어 지정
CMD ["java", "-jar", "05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar", "--spring.profiles.active=dev"]
## Project-MAD
  
### 목차
1. 프로젝트 개요
2. 아키텍처
3. 개발 환경
4. 테스트 환경
5. 설치
6. 운영 가이드 
#

  
  
#### 1. 프로젝트 개요
```
  Migration

  Assessment

  Discovery
```

#### 2. 아키텍처
  
- 시스템 아키텍처
  
<img
  src="https://user-images.githubusercontent.com/80949282/193211555-11c0a301-30da-4414-ad52-d1524313c967.png"
  width="70%"
  height="70%"
/>
  
- 소프트웨어 아키텍처
  
<img
  src="https://user-images.githubusercontent.com/80949282/193211585-78b12c8d-014a-4fe5-8992-c3a16d0f57a9.png"
  width="70%"
  height="70%"
/>
  
  
#### 3. 개발 환경
  
- 개발 언어 및 프레임워크
  - Front-end : Javascript, React, VsCode
  - Back-end : Java, SpringBoot, STS/Intelli-J
  - Discovery : Java, Maven, STS
  - Database : MySQL
  
  
- 소스코드 관리
  - Github -> https://github.com/mzc-mmc  
  ![image](https://user-images.githubusercontent.com/80949282/193714411-452d6508-8a7c-499a-87be-8bd8b4f3aa78.png)

  - Github Repositories
  ![image](https://user-images.githubusercontent.com/80949282/193714450-26ebbcdb-d996-42a0-9eea-6985310765dd.png)




#### 4. 테스트 환경
  
- 테스트 대상 서버 
  - 대표적인 리눅스 서버 6개 버전에 대하여 테스트 진행
  - EC2 instance로 구동중이며 public IP 접근
  - 기본적인 host 정보와 application을 순차적으로 접근하여 개발 진행 중


- Jenkins 배포

<img
  src="https://user-images.githubusercontent.com/80949282/193716504-d379c995-5e9b-4d18-9691-7ff4ab20bf4e.png"
  width="50%"
  height="50%"
/>
  
  -> http://43.200.26.111:8080/  
![image](https://user-images.githubusercontent.com/80949282/193714323-5f2d6659-4509-4fd8-9561-8f2566fe18db.png)

  
#### 5. 설치

- Ansible 배포

<img
  src="https://user-images.githubusercontent.com/80949282/193716640-12df3c51-253a-4bc4-85fc-854aa3d21721.png"
  width="50%"
  height="50%"
/>
  
  
#### 6. 운영 가이드
  
- Project MAD -> http://3.34.81.239/
  ```
  개발 진행 상황 (2022.09.30 기준)
  - 기본적인 UI 프레임 구성 (완료)
    - Target Host 화면
    - Host Info 화면
    - Application Info 화면
  - API 프레임 구성 (완료)
    - 10개 API (Swagger 참조)
  - Disocvery 엔진 구성 (완료)
    - Host 기본정보, Account 정보, Schedule 정보, Usage 정보, Application 구성 정보

  향후 진행 예정
  - 각 화면의 목록에서 상세페이지 구현 (2-depth)
  - 대시보드 및 UI 디자인 보완
  - 기타 필요한 화면 및 기능 추가 구현
  ```
  
- API 관리 : Swagger UI -> http://3.34.81.239:8080/swagger-ui/index.html
 ![image](https://user-images.githubusercontent.com/80949282/193715209-d2e1657e-4730-4f87-baa7-fe9715bd4d49.png)
  
  
- Target host
  - 수집 대상 시스템의 목록을 관리하는 화면
  - 엑셀 템플릿 시트 다운로드 및 엑셀 업로드로 대상 시스템을 관리
  - 대상 시스템은 Linux, Unix, Windows이며 현재는 Linux를 대상으로 구현되어 있음
  - 상세 페이지 전환시 요구되는 기능 및 화면
    - 대상 호스트의 등록 및 수정 등의 업데이트 이력
    - 대상 호스트의 수집 이력
    
  ![image](https://user-images.githubusercontent.com/80949282/193715277-e46bb540-f486-4ca9-945a-46e3f96a8e11.png)
  
- Host Info
  - Host의 IP address를 기준으로 기본적인 정보를 수집한 결과를 관리
  - 상세 페이지 전환시 요구되는 기능 및 화면
    - 데상 호스트의 Account 정보, 시스템 Usage 정보 (CPU, Memory, Disk volume)
    - 대상 호스트의 Application 정보

  
  ![image](https://user-images.githubusercontent.com/80949282/193715387-dee35680-2d41-44e2-adf3-9e31c71f2c4c.png)
  
- Application Info
  - Host의 IP address를 기준으로 수집 시간 기준의 활동중인 프로세스를 수집
  - 잘 알려진 Solution 또는 언어 기반으로 분류

  
  ![image](https://user-images.githubusercontent.com/80949282/193715409-bcbb4d1f-c171-456e-8510-07dedd6568b2.png)
  
  


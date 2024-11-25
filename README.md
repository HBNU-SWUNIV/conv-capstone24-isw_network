
# **한밭대학교 인공지능소프트웨어학과 iSW_network팀** 

- **팀 구성**
  
  - 20221075 정현서 
  - 20221046 김서연  
  - 20231081 한재웅


  
## Teammate Project Background

- **필요성**
  - 모바일 플랫폼에 따른 이동성과 접근성 향상
  - 즉각적인 상호작용과 소셜 경험 제공
  - 다양한 게임 선택을 통한 사용자 만족도 향상
  - 기술적 도전과 멀티 플레이어 기술 역량 강화

- **기존 해결책의 문제점**
  - 기존 싱글 플레이 게임은 사용자 간 실시간 상호작용 기능 부재로 인해 몰입감이 낮음
  - 멀티플레이 게임이 제공되더라도 서버와 클라이언트 간의 원활한 통신을 유지하기 어려움
  - 다양한 미니게임을 한 플랫폼 내에서 자유롭게 선택할 수 있는 유연한 구조의 애플리케이션 부족

## System Design

### System Requirements

- **Photon Engine**
  - **Photon Unity Networking (PUN)**: 멀티플레이어 게임용 유니티 패키지
  - 본 프로젝트에서는 PUN을 사용하여 게임의 서버와 클라이언트 간 실시간 통신을 관리하고 멀티 플레이어 환경을 구현
  - Photon을 활용해 게임 룸 생성 및 참여, 실시간 게임 동시 진행, 멀티 플레이어 매칭 시스템을 효과적으로 처리
  - 플레이어들은 Photon 서버와 연결하여 다른 사용자들과 동기화된 상태에서 게임을 진행

- **로비 화면**
  - Photon Engine을 사용하여 안정적인 네트워크 연결과 실시간 멀티플레이 구현
  - 사용자 식별이 가능한 로그인 기능
  - 방 생성·방 랜덤 참여·생성되어 있는 방 목록 확인 후 원하는 방에 참여할 수 있는 기능 ( 방 생성 시 방장이 방 제목과 최대 참여 인원을 직접 설정 )
  - 게임 시작 조건으로는 방에 들어온 모든 플레이어가 준비 완료 상태이어야만 방장이 게임을 시작할 수 있도록 설정

- **게임 선택 화면**
  - 총 4가지의 게임 선택 가능
  - 방장에게만 게임 선택 버튼과 돌아가기 버튼의 선택 권한을 부여하여 멀티플레이 환경에서의 관리와 운영을 효과적으로 분리
 
- **게임 화면**
  - 실시간으로 동시 진행
  - Click Click : 제한시간 15초 간 Click을 많이 터치한 플레이어 우승
  - Number Matching : 제한시간 15초 간 1부터 25까지의 숫자를 순서대로 빨리 클릭한 플레이어 우승
  - Speed Tap : Click을 가장 재빠르게 클릭한 플레이어 우승
  - Random Game : 위 3가지의 게임 중 한 게임이 랜덤으로 실행

- **리더보드 화면**
  - 게임 종료 이후 함께 플레이한 플레이어들의 리더보드를 표시

### System Configuration Diagram

- 클라이언트와 서버 간의 통신 흐름 및 네트워크 구조를 나타낸 시스템 구성도

<img width="723" alt="image" src="https://github.com/user-attachments/assets/9266ecea-d541-4d51-93e0-9e700a5efab2">



## Case Study

### Description

- **프로젝트 개요**
  - Unity와 Photon Engine을 사용하여 모바일 플랫폼에서 멀티플레이 시스템을 구현하는 사례로 다양한 미니게임을 실시간으로 다른 사용자와 즐길 수 있도록 설계됨
  - 사용자는 하나의 애플리케이션 내에서 다양한 미니게임을 선택하여 즐길 수 있으며 각 게임은 네트워크를 통해 실시간으로 동기화되어 사용자 간 상호작용이 원활하게 이루어짐

- **사용 기술 및 선정 이유**
  - **Unity**: 다양한 플랫폼 호환성을 제공하고 직관적인 개발 환경과 네트워크 기능이 우수하여 멀티플레이 시스템 구축에 적합한 도구로 선택
  - **Photon Engine**: PUN을 통해 서버와 클라이언트 간의 통신 및 멀티플레이 기능 구현 가능
  - **모바일 플랫폼**: 게임 접근성이 좋으므로 선택

- **프로젝트 결과 이미지**
  - **로비 화면**

  <img width="723" alt="image" src="https://github.com/user-attachments/assets/5c14dc8d-7e42-41ad-a7f4-19b248ffcf88">


  - **게임 선택 화면**
    
  <img width="200" alt="image" src="https://github.com/user-attachments/assets/653583c1-53e7-4ea7-bee5-0e182cdc5f6b">


  - **게임 화면**

  <img width="723" alt="image" src="https://github.com/user-attachments/assets/6e6a1e22-77a5-45e8-8286-24a3bcaacf8b">


  - **리더보드 화면** : Speed Tap의 리더보드
 
  <img width="200" alt="image" src="https://github.com/user-attachments/assets/16ce1c1f-6d51-49c5-b059-1dc9de49921e">

  - **SW 설치 매뉴얼**
    1. macOS에서 App Store를 열고 Xcode를 검색하여 설치한다.
    2. iOS 기기를 USB 케이블을 사용하여 macOS와 연결한다.
    3. 만든 프로젝트의 Unity에서 File -> Build Settings를 열고 프로젝트 창에서 Lobby-GameSelect-RandomGame-Game1-Game2-Game3-Leaderboard-Scenes/SampleScene 순으로 드래그앤 드롭한다.
    4. 좌측 하단의 Player Settings를 클릭하고 Project Settings 창에서 Company Name에 다른 사람과 등록 이름이 겹치지 않도록 이름을 입력한다.
    5. 창을 끄고 Build Settings로 돌아와서 Build 버튼을 클릭하여 빌드를 실행한다.
    6. 새로운 폴더를 만들고 만들어진 폴더를 저장 경로로 지정한다.
    7. 빌드가 완료되면 저장된 폴더가 나타나는데 그중 Unity-iPhone.xcodeproj를 더블 클릭하면 Xcode가 실행된다.
    8. Xcode가 실행되면 좌측 상단의 Unity-iPhone을 클릭하고 Signing & Capabilities를 클릭한 후 Automatically manage signing을 체크한다.
    9. 그 아래의 Add Account를 클릭하여 본인의 Apple ID를 입력하고 Next를 클릭 후 나타나는 입력 창에 패스워드를 입력한다.
    10. Xcode 화면으로 돌아온 뒤 Team에서 방금 등록한 계정을 선택한다.
    11. 화면 상단의 Unity-iPhone의 우측을 클릭하고 연결한 아이폰을 선택한다.
    12. 선택 후, 화면 상단의 실행 버튼을 누르면 설치가 시작된다. 설치 시 화면이 꺼지지 않게 해야한다.
    13. 설치 완료 시 실행이 되지 않는다면, 기기에서 설정 -> 일반 -> VPN 및 기기 관리에서 등록한 후 재실행하면 된다.



## Conclusion

- **멀티플레이 시스템 구축의 성공적인 구현**
  - Unity와 Photon Engine을 활용하여 모바일 플랫폼에서의 멀티플레이 시스템을 성공적으로 구현
  - 다양한 미니게임을 자유롭게 선택하고 실시간으로 즐길 수 있는 환경을 제공하여 사용자 간 몰입감을 높임

- **기술적 성과와 배운 점**
  - PUN을 통해 서버와 클라이언트 간의 복잡한 멀티플레이어 시스템 설계를 이해하게 됨

- **향후 개선 및 확장 방안**
  - 게임의 다양성을 향상시키려 함
  - 다양한 모바일 플랫폼에서도 동작할 수 있도록 할 계획

- **프로젝트의 의의**
  - 본 프로젝트는 멀티플레이 시스템 개발과 실시간 통신 기술에 대한 실용적 이해를 높이는 경험을 제공했으며 사용자 중심의 상호작용과 몰입감을 강화하는 멀티플레이어 시스템의 중요성을 확인함


## 파일 링크
- [파일 다운로드](https://drive.google.com/file/d/1WPXKfwWyo0dItPZRrnOvTtpYlphxlcAL/view?usp=sharing)

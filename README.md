<img width="638" alt="image" src="https://github.com/user-attachments/assets/3abe94cd-d0bd-4de7-a053-5d7a1446178f"># 한밭대학교 인공지능소프트웨어학과 iSW_network팀

**팀 구성**
- 한밭대학교 인공지능소프트웨어학과 김은경 교수님
- 20221075 정현서
- 20221046 김서연
- 20231081 한재웅

  
## Teammate Project Background

- **필요성**
  - 모바일 플랫폼에서 사용자가 언제 어디서나 쉽게 접근할 수 있는 **멀티플레이 게임**에 대한 수요 증가
  - 다양한 미니게임을 하나의 애플리케이션에서 **자유롭게 선택하고 플레이**할 수 있는 환경이 필요함
  - **실시간 상호작용**을 통해 사용자 간의 몰입감 있는 게임 경험을 제공함으로써, **유저 만족도 향상**

- **기존 해결책의 문제점**
  - 기존 싱글 플레이 게임은 **사용자 간 실시간 상호작용 기능 부재**로 인해 몰입감이 낮음
  - 멀티플레이 게임이 제공되더라도, **서버와 클라이언트 간의 원활한 통신을 유지하기 어려움**
  - 다양한 미니게임을 한 플랫폼 내에서 자유롭게 선택할 수 있는 **유연한 구조의 애플리케이션 부족**

## System Design

### System Requirements

- **멀티플레이어 기능 구현**
  - 다수의 사용자가 동일한 네트워크 서버에 접속하여 **실시간으로 참여**할 수 있어야 함
  - **Photon Engine**을 이용하여 서버와 클라이언트 간의 원활한 통신을 지원하고, 서버 측에서 다수의 플레이어 연결을 안정적으로 관리할 수 있어야 함
  - 서버와 클라이언트 간의 통신이 **실시간으로 동기화**되어 사용자 간의 상호작용이 지연 없이 진행되어야 함

- **게임 룸 생성 및 참여 기능**
  - 사용자가 **게임 룸을 생성**하거나 기존의 룸에 **참여**할 수 있는 기능을 제공해야 함

- **다양한 미니게임 선택 기능**
  - 애플리케이션 내에서 여러 종류의 **미니게임을 선택할 수 있는 인터페이스**가 필요함
  - 사용자는 앱 내에서 제공되는 미니게임 중 하나를 선택하여 자유롭게 플레이할 수 있어야 하며, 각 게임에 대한 **접근성과 사용성이 용이**해야 함
  - 미니게임들은 **서버-클라이언트 구조로 구현**되어야 하며, 모든 게임이 동일한 서버 내에서 원활히 작동할 수 있도록 최적화되어야 함

- **Photon Engine의 최적화 및 확장성**
  - **Photon Unity Networking (PUN)**을 사용하여 멀티플레이어 게임 환경을 최적화하고, 추후에 게임 콘텐츠를 확장할 수 있도록 시스템을 구성해야 함
  - Photon 서버를 통해 **사용자 간 원활한 통신과 동기화**가 가능하며, 서버 부하 관리와 확장성을 고려한 설계가 필요함
  - 멀티플레이 환경 내에서 게임 룸 관리, 실시간 데이터 송수신, 대규모 사용자 동시 접속 등의 요구 사항을 충족할 수 있어야 함

## 시스템 구성도

- 아래는 본 프로젝트의 **시스템 구성도**입니다. 클라이언트와 서버 간의 통신 흐름 및 네트워크 구조를 시각적으로 보여줍니다

![image](https://github.com/user-attachments/assets/cf0ebac0-f4fe-481b-a932-0ff6e0b7f8dc)


## Case Study

### Description

- **프로젝트 개요**
  - Unity와 Photon Engine을 사용하여 모바일 플랫폼에서 **멀티플레이 시스템을 구현**하는 사례로, 다양한 미니게임을 실시간으로 다른 사용자와 즐길 수 있도록 설계됨
  - 사용자는 하나의 애플리케이션 내에서 다양한 미니게임을 선택하여 즐길 수 있으며, 각 게임은 **네트워크를 통해 실시간으로 동기화**되어 사용자 간 상호작용이 원활하게 이루어짐

- **사용 기술 및 선정 이유**
  - **Unity**: 다양한 플랫폼 호환성을 제공하고 직관적인 개발 환경과 네트워크 기능이 우수하여 멀티플레이 시스템 구축에 적합한 도구로 선택됨
  - **Photon Engine**: PUN을 통해 서버와 클라이언트 간의 **실시간 통신**을 쉽게 구현해 몰입감 있는 게임 경험을 제공함
  - **모바일 플랫폼**: 언제 어디서나 멀티플레이 게임을 즐길 수 있도록 모바일 플랫폼을 선택

- **구현 기능과 사례**

  <img width="632" alt="image" src="https://github.com/user-attachments/assets/7292f8cb-5806-4c29-8e05-514275d9d644">
  
  - **멀티플레이어 매칭 및 게임 룸 생성**: 사용자가 게임 룸을 생성하거나 기존 룸에 참여할 수 있어 다른 플레이어들과 함께 게임 가능
    
  <img width="638" alt="image" src="https://github.com/user-attachments/assets/4d830d63-ee4b-487f-aac6-e8cf73b798c2">

  - **다양한 미니게임 제공**: 여러 미니게임을 선택할 수 있어, 사용자가 다양한 콘텐츠를 경험할 수 있도록 설계됨


## Conclusion

- **멀티플레이 시스템 구축의 성공적인 구현**
  - Unity와 Photon Engine을 활용하여 **모바일 플랫폼에서의 멀티플레이 시스템을 성공적으로 구현**
  - 다양한 미니게임을 자유롭게 선택하고 실시간으로 즐길 수 있는 환경을 제공하여 사용자 간 몰입감을 높임

- **기술적 성과와 배운 점**
  - PUN을 통해 서버와 클라이언트 간의 복잡한 멀티플레이어 시스템 설계를 이해하게 됨
  - 네트워크 불안정 상황에서의 자동 재연결 및 오류 복원 기능을 통해 **안정적인 네트워크 환경 유지의 중요성**을 학습함

- **향후 개선 및 확장 방안**
  - **새로운 미니게임과 게임 모드 추가**를 통해 사용자 경험을 풍부하게 하고자 하며, 안정적인 서버 관리를 통해 **원활한 멀티플레이 환경**을 제공할 계획
  - AI 봇 도입 및 데이터 분석을 통해 사용자 맞춤형 게임 환경을 제공하는 등의 **확장성 및 사용자 맞춤 기능** 개발 목표 설정

- **프로젝트의 의의**
  - 본 프로젝트는 **멀티플레이 시스템 개발과 실시간 통신 기술에 대한 실용적 이해**를 높이는 경험을 제공했으며, 사용자 중심의 상호작용과 몰입감을 강화하는 멀티플레이어 시스템의 중요성을 확인함




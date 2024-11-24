
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

- **멀티플레이어 기능 구현**
  - 다수의 사용자가 동일한 네트워크 서버에 접속하여 실시간으로 참여할 수 있어야 함
  - Photon Engine을 이용하여 서버와 클라이언트 간의 원활한 통신을 지원하고 서버 측에서 다수의 플레이어 연결을 안정적으로 관리할 수 있어야 함
  - 서버와 클라이언트 간의 통신이 실시간으로 동기화되어 사용자 간의 상호작용이 지연 없이 진행되어야 함

- **게임 룸 생성 및 참여 기능**
  - 사용자가 게임 룸을 생성하거나 기존의 룸에 참여할 수 있는 기능을 제공해야 함

- **다양한 미니게임 선택 기능**
  - 애플리케이션 내에서 여러 종류의 미니게임을 선택할 수 있는 인터페이스가 필요함
  - 사용자는 앱 내에서 제공되는 미니게임 중 하나를 선택하여 자유롭게 플레이할 수 있어야 하며 각 게임에 대한 접근성과 사용성이 용이해야 함
  - 미니게임들은 서버-클라이언트 구조로 구현되어야 하며 모든 게임이 동일한 서버 내에서 원활히 작동할 수 있도록 최적화되어야 함

- **Photon Engine**
  - **Photon Unity Networking (PUN)**: 멀티플레이어 게임용 유니티 패키지
  - 본 프로젝트에서는 PUN을 사용하여 게임의 서버와 클라이언트 간 실시간 통신을 관리하고 멀티 플레이어 환경을 구현
  - Photon을 활용해 게임 룸 생성 및 참여, 실시간 게임 동시 진행, 멀티 플레이어 매칭 시스템을 효과적으로 처리
  - 플레이어들은 Photon 서버와 연결하여 다른 사용자들과 동기화된 상태에서 게임을 진행



## 시스템 구성도

- 아래는 본 프로젝트의 클라이언트와 서버 간의 통신 흐름 및 네트워크 구조를 나타낸 시스템 구성도

![image](https://github.com/user-attachments/assets/9266ecea-d541-4d51-93e0-9e700a5efab2)



## Case Study

### Description

- **프로젝트 개요**
  - Unity와 Photon Engine을 사용하여 모바일 플랫폼에서 멀티플레이 시스템을 구현하는 사례로 다양한 미니게임을 실시간으로 다른 사용자와 즐길 수 있도록 설계됨
  - 사용자는 하나의 애플리케이션 내에서 다양한 미니게임을 선택하여 즐길 수 있으며 각 게임은 네트워크를 통해 실시간으로 동기화되어 사용자 간 상호작용이 원활하게 이루어짐

- **사용 기술 및 선정 이유**
  - **Unity**: 다양한 플랫폼 호환성을 제공하고 직관적인 개발 환경과 네트워크 기능이 우수하여 멀티플레이 시스템 구축에 적합한 도구로 선택
  - **Photon Engine**: PUN을 통해 서버와 클라이언트 간의 통신 및 멀티플레이 기능 구현 가능
  - **모바일 플랫폼**: 게임 접근성이 좋으므로 선택

- **구현 기능과 사례**

    <img width="723" alt="image" src="https://github.com/user-attachments/assets/83af9f4f-f381-426e-824a-9bce03545cac">

  - **멀티플레이어 매칭 및 게임 룸 생성**: 사용자가 게임 룸을 생성하거나 생성된 룸에 참여할 수 있어 다른 플레이어들과 함께 게임 가능
    
  <img width="723" alt="image" src="https://github.com/user-attachments/assets/4d830d63-ee4b-487f-aac6-e8cf73b798c2">

  - **다양한 미니게임 제공**: 사용자가 직접 원하는 미니게임을 선택하여 즐길 수 있도록 설계


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

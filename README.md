# 한밭대학교 인공지능소프트웨어학과 iSW_network팀

## 팀 구성
- **지도교수**
  - 김은경 교수님
- **팀원**
  - 20221075 정현서
  - 20221046 김서연
  - 20231081 한재웅

## 프로젝트 주제
- 네트워크 기반 멀티플레이 시스템 구현

## 프로젝트 설명
- 본 프로젝트는 **Unity**를 이용하여 **모바일 플랫폼**에서 멀티플레이 시스템을 구현하는 것을 목표로 합니다. 이 애플리케이션은 사용자가 다양한 미니게임을 하나의 앱에서 자유롭게 선택하고, 다른 사용자와 네트워크를 통해 실시간으로 게임을 즐길 수 있는 기능을 제공합니다. **Unity**는 다양한 플랫폼에 호환성을 제공하며, 직관적인 개발 환경과 풍부한 네트워크 기능을 통해 멀티플레이 시스템 구축에 적합하기 때문에 사용되었습니다. 또한, **Photon Engine**을 사용하여 서버와 클라이언트 간의 실시간 통신을 구현합니다. 이를 통해 사용자 간 상호작용을 강화하고 몰입감 있는 게임 경험을 제공하는 것을 목표로 합니다.

## 플랫폼 및 개발 툴
- **플랫폼**: 모바일
- **개발 툴**: Unity

## 주요 기능
- 다수의 사용자가 네트워크 서버를 통해 실시간으로 참여할 수 있는 멀티플레이어 기능을 제공합니다.
- 다양한 미니게임을 사용자들이 자유롭게 선택하여 플레이할 수 있습니다.

## 목표
- 언제 어디서든 쉽게 즐길 수 있는 자유로운 멀티 플레이 미니게임을 제공합니다.

## 개발 필요성
- 이동성과 접근성을 향상합니다.
- 즉각적인 상호작용과 소셜 경험을 제공합니다.
- 다양한 게임 선택을 통해 사용자 만족도를 향상합니다.
- 기술적 도전과 멀티플레이어 기술 역량을 강화합니다.

## 개발 목적
- 모바일 게임을 제공함으로써, 사용자가 언제 어디서나 편리하게 다양한 게임을 즐길 수 있도록 합니다.
- 친구와 함께 플레이할 수 있는 멀티 플레이 기능을 통해 게임의 재미를 증가시킵니다.
- 사용자 간 상호작용과 경쟁을 촉진하여 게임의 몰입도를 높이고 즐거움을 제공합니다.

## 세부 기능 - 멀티플레이
1. **게임 룸 생성 및 참여**
   - 사용자는 자신만의 게임 룸을 생성하거나 기존의 룸에 참여할 수 있습니다.
   - 랜덤 룸 참여 기능을 통해 사용자가 다른 플레이어와 매칭되어 게임을 즐길 수 있습니다.
   - 플레이어 수와 게임 종류를 직접 선택할 수 있습니다.

2. **실시간 게임 동시 진행**
   - 게임은 실시간으로 진행되며, 서버와 클라이언트 간의 통신을 통해 게임 상태가 동기화됩니다.
   - 플레이어들은 각자의 장치에서 실시간으로 게임을 진행하며, 진행 상황과 결과는 자동으로 업데이트됩니다.

## 시스템 구성도
- 아래는 본 프로젝트의 시스템 구성도를 시각화한 이미지입니다. 이 구성도는 시스템 내에서 클라이언트와 서버 간의 통신 흐름 및 네트워크 구조를 보여줍니다.
<img width="263" alt="image" src="https://github.com/user-attachments/assets/9caccbd5-d760-4159-b9f7-6c2ffa9fff48">


## 적용 기술 – Photon Engine
- **Photon Unity Networking (PUN)**: Photon Engine은 멀티플레이어 게임을 위한 오픈소스 네트워크 엔진입니다. PUN을 통해 Unity 기반의 게임에서 서버와 클라이언트 간의 실시간 통신을 쉽게 구현할 수 있습니다.
   - 본 프로젝트에서는 PUN을 활용하여 실시간 멀티플레이어 환경을 구축했습니다. 이를 통해 사용자는 다른 사용자와 네트워크를 통해 게임에 참여하고 상호작용할 수 있으며, 게임 룸 생성과 참여, 실시간 동기화, 멀티플레이어 매칭 등의 기능을 제공받을 수 있습니다.
   - Photon 서버와의 연결을 통해 사용자 간의 원활한 통신이 가능하며, 이를 통해 동기화된 상태에서 멀티플레이 게임이 진행됩니다.

## 프로젝트 성과
- 2024년 오픈소스경진대회 참가

## 파일 링크
- [파일 다운로드](https://drive.google.com/file/d/1WPXKfwWyo0dItPZRrnOvTtpYlphxlcAL/view?usp=sharing)


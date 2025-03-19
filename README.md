https://chhplus.hanwha.com/web/you/youMain.do

1. JAUS 개요 및 필요성

1.1 JAUS란?

JAUS(Joint Architecture for Unmanned Systems)는 무인 시스템의 상호 운용성을 보장하기 위한 개방형 표준으로, 다양한 무인 플랫폼 간의 통신 및 제어를 표준화하는 것을 목표로 합니다. 
SAE(미국자동차공학회)의 AS-4 위원회에서 관리하며, 방위산업 및 산업 자동화 등에서 활용되고 있습니다.

1.2 JAUS의 필요성

이종 시스템 간 상호 운용성: 다양한 무인 시스템(로봇, 드론, 무인 차량 등) 간의 통신을 표준화하여 시스템 통합을 용이하게 함.
비용 절감 및 개발 시간 단축: 표준화된 인터페이스를 사용함으로써 개발자가 개별적인 맞춤형 프로토콜을 설계할 필요 없음.
유지보수 및 확장성 확보: 공통 표준을 따르므로 향후 시스템 확장 및 유지보수가 용이.

2. JAUS 아키텍처 및 핵심 개념

2.1 JAUS의 계층적 구조
JAUS는 모듈화된 구조를 가지며, 주요 계층은 다음과 같습니다:
Application Layer: 사용자가 정의한 응용 서비스
Communications Layer: 메시지 송수신 및 데이터 관리
Transport Layer: 물리적 통신 방법(UDP, TCP, 시리얼 등)

2.2 JSIDL(JAUS Service Interface Definition Language)
JSIDL은 JAUS 서비스 인터페이스를 정의하는 XML 기반의 언어로,
메시지 구조 정의
데이터 형식 및 유효성 검사
서비스 상호작용 및 상태 머신 정의 등을 포함합니다.


2. JAUS의 핵심 기술 요소
SOA (Service-Oriented Architecture) 기반 설계
비동기식 메시지 통신 (Message-based Communication)
계층적 모듈화 (Hierarchical Modular Design)
하드웨어/네트워크 독립성 (Hardware & Network Agnostic Design)

4. JAUS의 표준 구조 및 계층별 역할
계층	기능 설명
Mobility	이동 플랫폼(UGV, UAV, USV 등) 제어
Manipulator & Payload	로봇 팔, 무기 시스템, 센서 등 장비 제어
Communications	데이터 전송 및 네트워크 관리 (무선/유선)
Human Interaction	원격 조종 및 HMI(Human-Machine Interface)
Mission Planning	자율주행, 임무 계획 및 고급 AI 알고리즘 적용

6. JAUS의 기술적 특징 심화 분석
(1) SOA(Service-Oriented Architecture) 기반 설계
JAUS는 **서비스 기반 아키텍처(SOA)**를 따르며, 각 기능이 독립적인 서비스로 구성됨
예제: 센서 데이터를 요청하면 JAUS 표준 메시지를 통해 필요한 정보만 전달됨

(2) 메시지 기반 비동기 통신 (Message-based Communication)
TCP/IP, RS232, CAN 등 다양한 네트워크에서 사용 가능
Request-Response & Publish-Subscribe 모델 지원
MIL-STD-6016, STANAG 4586 같은 군용 데이터 표준과도 호환

(3) 데이터 버스 설계 및 실시간 운영
JAUS는 **RTOS(Real-Time Operating System)**에서 동작 가능
UAV, UGV와 같은 임무 수행 중 실시간성을 유지하는 구조적 장점


고찰 및 시사점

방산분야에서 JAUS를 사용하는 이유

1. 이종 시스템 간 상호 운용성 (Interoperability)
다양한 무인 플랫폼(UGV, UAV, USV 등)과의 원활한 통신 및 제어를 가능하게 하여 전장 환경에서의 통합 운용을 지원함.
NATO STANAG 4586 및 MIL-STD-6016 등과의 호환성을 제공하여 기존 군용 데이터 표준과 연계 가능.
2. 모듈화 및 확장성 (Modular & Scalable Architecture)
SOA(Service-Oriented Architecture) 기반으로 설계되어 신규 시스템 추가 및 기능 확장이 용이함.
특정 임무나 하드웨어 변화에 맞춰 소프트웨어를 변경할 수 있어 재사용성이 높음.
3. 표준화된 인터페이스 (Standardized Interface)
방위산업에서는 신뢰성 있는 표준을 준수하는 것이 필수적이며, JAUS는 SAE AS5684A 표준을 따름.
이를 통해 방산 기업 및 정부 기관이 일관된 개발 및 유지보수 프로세스를 수행 가능.
4. 실시간성 미보장에도 불구하고 적용되는 이유
JAUS는 하드 리얼타임 시스템을 보장하지 않지만, RTOS(Real-Time Operating System)와 함께 사용할 경우 일정 수준의 실시간성을 확보 가능.
실제 전장 환경에서는 완전한 하드 리얼타임이 아닌, 페일 세이프(Fail-Safe) 및 페일 소프트(Fail-Soft) 설계가 중요하며, JAUS는 이를 지원하는 구조를 가짐.
무기체계의 센서 퓨전, 자율 임무 수행, 원격 조종 등의 다양한 시나리오에서 상황별 실시간성 조절이 가능하도록 설계됨.
5. 비용 절감 및 개발 효율성 향상
신규 무인 시스템을 개발할 때 맞춤형 프로토콜을 설계할 필요 없이 JAUS 표준을 활용하여 개발 시간과 비용을 절감할 수 있음.
군사 시스템은 장기 운영 및 유지보수가 필수적인데, JAUS의 표준화된 구조 덕분에 유지보수와 업그레이드가 용이함.



JAUS는 하드 리얼타임을 보장하지 않음에도 불구하고 방산 분야에서 널리 사용되는 이유는 확장성과 상호 운용성 때문임.
미군과 NATO 국가들은 다양한 무인 시스템을 운영해야 하며, 이를 하나의 네트워크로 통합하기 위해 JAUS를 적극 활용하고 있음.


장/단점

장점
상호 운용성 보장: 동일한 메시지 세트를 사용하는 다양한 도메인 및 무인 시스템 간에 상호 운용성을 보장합니다.
모듈성: 하위 시스템을 소프트웨어 구성 요소로 분할하는 계층적 아키텍처를 통해 모듈성을 보장합니다.
소프트웨어 재사용 가능: JAUS 구성 요소의 소프트웨어 재사용이 가능합니다.

단점
주소 할당의 비명시적 정의: 주소 할당 방법이 명시되지 않아 각 노드에 수동으로 전역 고유 식별자를 할당해야 합니다.
엄격한 메시지 정의: 특정 기능을 제공하는 구성 요소가 구현해야 하는 메시지를 엄격하게 정의하여 시스템 빌더의 자유를 제한할 수 있습니다.
실시간 요구 사항에 대한 지침 부족: 실시간 요구 사항에 대한 지침을 제공하지 않습니다.
상호 운용성 저하: 여러 시스템이 함께 작동하기 위해 일부 수동 구성이 필요하여 상호 운용성을 저하시킵니다.


https://openjaus.com/wp-content/uploads/2017/06/1545-Robotic_Manipulation_and_Haptic_Feedback_via_High_Speed_Messaging_with_JAUS.pdf
https://wiki.robojackets.org/images/1/13/Reference_Architecture%2C_Part_1%2C_V3-3.pdf
https://openjaus.com/understanding-jaus/
https://en.wikipedia.org/wiki/JAUS

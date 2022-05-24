# Tech-Interview
📢🙍 기술 면접 준비용 자료 저장소입니다(수정중).

# 1. Basics of Cloud Service

## 1-1. On-Premise와 Cloud 차이
- On-Premise
  - `+`: 강력한 보안 / 맞춤형 하드웨어 / 데이터 가시성 및 관리
  - `-`: 초기 투자 비용 / 한정된 컴퓨팅 파워 / 인력 투자 / 
- Cloud 
  - `+`: 변화에 신속, 탄력 / 인프라 운영대신 비즈니스에 집중 / 비용 절감 사례 많음
  - `-`: 보안, 가시성 우려 / 지속적인 비용 / 

## 1-2. 퍼블릭 클라우드 vs 프라이빗 클라우드
리소스 공유, 관리, 효율적 / 가상화 , 자동화 / 종량제
Public : 인터넷 제공업체 / 수요변동에 탄력적 / Azure, GCP, AWS
Private : 인프라 내부적 운용 / 보안강점 / 리소스 통제 / 비용
Hybrid : VPN, P2P 연결 / 트래픽 급증시 퍼블릭에서 당겨옴 / 

## 1-3. AWS, GCP, Azure의 차이점 및 특징(Gartner, 9월)
AWS : 광범위한 영향력 / 제품간 결합 미흡
GCP : 오픈소스(K8s, Tensorflow) 파워 / 대기업 대응 부족
Azure : 완벽한 엔드 투 엔드(Oracle, SAP), 비용, Winserver / 가용성 영역 비율 낮음

# 2. Development

## 2-1. 2티어 / 3티어의 차이점
프레젠테이션(WEB) / 애플리케이션(WAS) / 데이터(DB)
2tier : (WEB + WAS) + DB / 개발편의성
3tier : WEB + WAS + DB / 확장성, 성능, 자원활용, 관리

## 2-2. ELK Stack 설명
모든 유형의 구조화 및 비정형 데이터에서 실시간 분석 도구
Elastic Search : 분산형 검색 및 분석 엔진
Logstash : 데이터 처리 파이프라인
Kibana : 데이터 시각화
Beats : 데이터 전송


# 3. Network

## 3-1. OSI 7계층 설명
네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것(통신 과정을 단계별로 파악)
Layer7 : 응용 / UI, Application
Layer6 : 표현 / 인코딩, 디코딩, 암호화
Layer5 : 세션 / 세션구축 및 관리
Layer4 : 전송 / TCP, UDP
Layer3 : 네트워크 / IP, ARP, RARP
Layer2 : 데이터링크 / MAC
Layer1 : 물리 / 전기적신호

## 3-2. TCP/IP 4계층 설명
Layer4(5,6,7) : 응용 / HTTP, FTP, Telnet, DNS, SMTP
Layer3(4) : 전송 / TCP, UDP
Layer2(3) : 인터넷 / IP, ARP, RARP,
Layer1(1,2) : 네트워크엑세스 / Ethernet, Token Ring, PPP

## 3-3. TCP / UDP 차이점
TCP : 연결형 프로토콜 / 1:1 통신방식 / 보안성이 높은 대신 UDP보다 전송속도가 느림 / 신뢰성
UDP : 비연결형 프로토콜 / 1:N, N:N 통신방식 / 보안성이 낮지만 속도가 빠름 / 스트리밍, VoIP

## 3-4. 3 Way Handshake, 4 Way Handshake
### 3 Way Handshake
SYN / 연결요청
SYN, ACK / 수락
ACK / 수락 확인

### 4 Way Handshake
FIN / 종료요청
ACK / 확인, 대기요청
FIN / 종료요청
ACK / 종료 확인

## 3-5. Bridge와 NAT 차이
NAT : 사설 IP -> 공인 IP / 공유기
Bridge : 사설 IP X / 호스트의 공인 IP와 같은 대역대 IP 사용

# 3-6. L4 vs L7
스위치로 들어온 패킷을 서버로 전송
L4 : IP + 포트 / 포트 기반 미러링 / 부하분산 특화, 고신뢰성
L7 : IP + 포트 + 페이로드 / 섬세, 고비용 / 컨텐츠 기반 트래픽 제어, QoS, 필터링, 패킷분석

# 4. Storage

## 4-1. NFS, LDAP, AD, DNS 설명
NFS : 썬마이크로 / 네트워크상 연결된 다른 PC 하드를 사용 / 중앙집중형
LDAP : DAP 경량 / TCP/IP 디렉토리 서비스 조회, 수정 프로토콜
AD : 계정, PC, 정책 정보 저장
DNS : 도메인 IP 변환 / 원래는 Hosts 파일 / root(.) – top-lv -second-lv - sub

# 5. Security

# 6. Database

# 7. DevOps
## 7-1. # Docker와 Kubernetes 차이점
Docker : 컨테이너 기반 오픈소스 가상화 플랫폼(개념) / 기술적 개념이자 도구
Kubernetes : 컨테이너 오케스트레이션 툴 / Docker를 관리하는 도구 / Docker Swarm, ECS, Nomad

## 7-2. Ansible을 사용하는 이유
IaC 지향 자동화 관리 도구 / Python 기반 YAML 포맷 Playbook 자동화 구현 / 단순, 편의, 멱등
Infrastructure as Code : 수동 대신 스크립트로 컴퓨팅 인프라 구성

## 7-3. 컨테이너 설명
애플리케이션 & 애플리케이션을 구동하는 환경을 격리한 공간 / OS 가상화 X 프로세스 격리

## 7-4. 오케스트레이션 설명
컨테이너를 스케쥴링 / 클러스터링 / 서비스 디스커버리 / 로깅 및 모니터링

## 7-5. IaaS, PaaS, SaaS의 차이점
Infrastructure(aaS) / HW 인프라 제공 / 빠른 변화 / AWS EC2, Azure, GCE
Platform(aaS) / 응용 SW 개발.운영 환경 제공 / 신속 개발 / Google App Engine, Openshift
Software(aaS) / 소프트웨어 제공 / 비즈니스 집중 / Google Apps, MS Office, Dropbox

## 7-6. DevOps, DevSecOps 설명
애자일에 개발과 운영 개선 및 자동화가 합쳐진 모델 / 개발, 배포 담당자들은 하나의 팀 / 개발과 배포를 서로 잘 융합시키고 소통을 원할하게 하기 위한 개발론
DevSecOps : 위 과정에 보안을 빌트인 / 파이프라인상에 유기적 결합 / 

# 8. Virtualization
## 8-1. VPN / VPC 설명
VPN : 가상의 사설망 / 실제로 같은 네트워크상이지만 논리적으로 다른 네트워크
VPC : 리소스간 허용 최소화 / 그룹별 네트워크 구성 용이


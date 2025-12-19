

## React/Next.js RSC 원격코드 실행 취약점 (CVE-2025-55182, CVE-2025-66478) 보고


### ㅁ 개요
- React / Next.js에서 치명적인 보안 취약점 CVE-2025-55182 (CVSS 10.0), CVE-2025-66478이 발견됨
- 본 취약점은 React 19의 React Server Components(RSC) 구현 과정에서 인증 절차 없이 서버의 제어권을 완전히 탈취 가능한 취약점이 확인되어 보고
* NVD의 경우 동일 취약점으로 판단하여 CVE-2025-55182로 중복(Duplicate)으로 처리


### ㅁ CVE-2025-55182 (React), CVE-2025-66478 (Next.js)

ㅇ 발생 원리 

- 이 취약점은 React 19의 핵심 기능인 **React Server Components (RSC)**가 클라이언트와 서버간에 데이터를 주고 받기 위해 사용하는 **Flight 프로토콜**의 처리 과정에서 발생

1. **직렬화 문제** : 공격자가 클라이언트에서 악의적으로 조작된 객체를 RSC 요청에 담아 서버로 전송

2. **검증 부재** : 서버 측 React 런타임(react-server-dom-webpack)이 데이터를 역직렬화하는 과정에서 입력값에 대한 타입 검증이 충분하지 않음
   
3. **코드 실행** : 공격자는 특정 내부 함수를 호출하도록 유도하여, Node.js의 **child_process**등을 실행시키고 **쉘 명령어**를 수행


ㅇ 영향도


### ㅁ 조치권고

- 자산확인

- 대상

- 취약한 버전 패치

- 점검 방법

### ㅁ 취약점 스캐너



### ㅁ IoC 정보

206[.]237.3.150, 2025-12-04, Earth Lamia

45[.]77.33.136, 2025-12-04, Jackpot Panda

143[.]198.92.82, 2025-12-04, Anonymization Network

183[.]6.80.214, 2025-12-04, 출처 불명 위협 클러스터

### ㅁ 대응방안


- IPS 차단 적용 완료

- 룰 설명

- 자산 확인 후 영향도 확인

- 제로데이 이전 로그들 확인


##### 출처


[NVD]
https://nvd.nist.gov/vuln/detail/CVE-2025-55182

[IoC]
https://aws.amazon.com/ko/blogs/security/china-nexus-cyber-threat-groups-rapidly-exploit-react2shell-vulnerability-cve-2025-55182/

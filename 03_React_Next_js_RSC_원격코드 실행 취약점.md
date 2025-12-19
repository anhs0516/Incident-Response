

## React/Next.js RSC 원격코드 실행 취약점 (CVE-2025-55182, CVE-202566478) 보고


### ㅁ 개요
- React / Next.js에서 치명적인 보안 취약점 CVE-2025-55182 (CVSS 10.0), CVE-2025-66478이 발견됨
- 본 취약점은 React 19의 React Server Components(RSC) 구현 과정에서 인증 절차 없이 서버의 제어권을 완전히 탈취 가능한 취약점이 확인되어 보고
* NVD의 경우 동일 취약점으로 판단하여 CVE-2025-55182로 중복(Duplicate)으로 처리


### ㅁ CVE-2025-55182 (React), CVE-2025-66478 (Next.js)

ㅇ 발생 원리 

- 

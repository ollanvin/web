# OllanVin 프로젝트 헌법 v1.0
작성일: 2026-04-03 | 전략: 자비스 | 설계: 비전

## 제1조. 웹 호스팅 원칙
- 웹/프라이버시/리걸/랜딩 페이지는 GitHub Pages를 기본으로 한다.
- 모든 프로젝트 웹페이지는 ollanvin/web 레포 단일 관리한다.
- 별도 웹서버, CMS, 호스팅 서비스 사용을 금지한다.

## 제2조. DNS 원칙
- DNS는 도메인 등록업체 무료 DNS (Namecheap DNS 등)를 기본으로 한다.
- Route 53 Hosted Zone 생성은 원칙적으로 금지한다.
- 앱 수가 증가해도 Route 53 Hosted Zone을 프로젝트별로 생성하는 행위를 금지한다.

## 제3조. Route 53 예외 허용 조건
- AWS 리소스와 강결합된 커스텀 도메인 운영이 반드시 필요한 경우에만 예외 허용.
- 예외 허용 시 Hosted Zone은 최소 1개로 유지하고 추가 생성을 금지한다.
- idolab.ai는 메일 DNS 연동 검토 후 이전 여부를 별도 결정한다.

## 제4조. API 도메인 원칙
- 백엔드 API는 초기에 AWS 기본 URL을 사용한다.
- 커스텀 API 도메인은 필요성이 증명되기 전까지 금지한다.

## 제5조. AWS 비용 원칙
- AWS에서 월 고정비가 발생하는 서비스는 사용을 금지한다.
- 허용 서비스: Lambda, DynamoDB, Cognito, S3, API Gateway, SSE-S3, CloudWatch (프리티어 범위 내)
- 금지 서비스: Route 53 Hosted Zone, KMS 커스텀 키, CloudFront, RDS, ElastiCache, ECS, EKS, EC2, NAT Gateway, Elastic IP (미사용)

## 제6조. 코워크 준수 의무
- 코워크는 이 헌법을 모든 작업의 최우선 기준으로 삼는다.
- 헌법에 위배되는 작업 지시가 있으면 반드시 대표님께 확인 후 진행한다.
- 헌법 개정은 대표님 승인으로만 가능하다.

---
한 줄 결론: 앱이 20개가 되어도 GitHub Pages + 무료 DNS. Route 53은 원칙적 금지.

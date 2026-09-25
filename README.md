# jjr-baecharyo — 조문 차량 배차표

장례(조문) 참석 시 차량 탑승 배차 안내 및 관리.

- **공개 배차표(조회용)**: https://cgn210-alt.github.io/jjr-baecharyo/funeral_transport.html
- **관리자**: https://cgn210-alt.github.io/jjr-baecharyo/admin.html

## 파일 구성

- `funeral_transport.html` — 공개 배차표. 로그인 없이 누구나 조회, 이름/부서/차량 검색 가능. 10초마다 자동 갱신.
- `admin.html` — 관리자 페이지. 로그인 후 장례 정보·차량별 탑승 인원을 수정하면 공개 배차표에 즉시 반영.

## 백엔드

Firebase Realtime Database (`cgn-love` 프로젝트, `baecharyo` 경로) 사용. 관리자 로그인은 Firebase Authentication(이메일/비밀번호).

## 배포

`사이트-올리기.bat` 더블클릭 → `git add / commit / push` 자동 실행 → GitHub Actions가 1~2분 내 자동 배포.

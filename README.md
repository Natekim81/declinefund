# 지역균형발전 사업검색

## Vercel 배포
1. 이 폴더를 GitHub 저장소에 업로드합니다.
2. Vercel에서 `Add New Project`를 선택합니다.
3. 해당 저장소를 Import합니다.
4. Framework Preset은 `Other`, Build Command는 비워 두고 배포합니다.

## 구조
- `index.html`: 검색·필터·사업 카드 UI
- `api/press.js`: korea.kr 보도자료 최신 목록 수집
- `public/cardnews.jpg`: 카드뉴스 이미지
- `vercel.json`: 보안 헤더 및 clean URL 설정

## 주의
대한민국 정책브리핑의 RSS 서비스는 중단되어 RSS 피드 자체를 직접 임베드할 수 없습니다.
대신 서버리스 함수가 보도자료 목록을 읽어 최신 5건 이상을 표시합니다.
korea.kr의 HTML 구조가 변경되면 `api/press.js`의 파싱 규칙을 조정해야 할 수 있습니다.

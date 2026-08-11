# sosocorp.io — 주식회사 소소컴퍼니 공식 홈페이지

정적 원페이지 사이트. 빌드 도구 없음 — `index.html` 하나에 HTML/CSS/JS가 전부 들어 있습니다.

## 수정하는 법

1. `index.html`을 편집합니다.
2. 브라우저로 파일을 그냥 열어 확인합니다. (또는 `python3 -m http.server 8000`)
3. 커밋 후 push 하면 GitHub Actions가 자동으로 배포합니다.

```bash
git add -A && git commit -m "내용 수정" && git push
```

## 확정된 회사 정보

- 상호: 주식회사 소소컴퍼니 / SOSO CORP.
- 사업자등록번호: 135-86-55936
- 주소: 서울시 서초구 사임당로8길 13, 4층 402호 엠432호
- 이메일: contact@sosocorp.io
- 설립: 2023년

## 아직 임시 문구인 곳

`index.html` 안에서 `TODO(` 로 검색하면 위치가 전부 나옵니다.

```bash
grep -n "TODO(" index.html
```

- 히어로 슬로건 / 설명 문구
- 회사 소개 2문단
- 사업영역 카드 3개 (제품 개발 / 데이터·자동화 / 컨설팅 — 개수 조정 가능)
- `<meta name="description">` 및 og 설명

## 도메인

- 배포: GitHub Pages
- 커스텀 도메인: `www.sosocorp.io` (`CNAME` 파일로 지정, HTTPS 강제 적용됨)
- DNS: 가비아

가비아 DNS 레코드 (설정 완료):

| 타입  | 호스트 | 값 |
|-------|--------|-----|
| A     | @      | 185.199.108.153 |
| A     | @      | 185.199.109.153 |
| A     | @      | 185.199.110.153 |
| A     | @      | 185.199.111.153 |
| CNAME | www    | `firefist123t6.github.io.` |

apex(`sosocorp.io`)는 GitHub이 받아서 `www`로 301 리다이렉트합니다.

## 디자인 토큰

색상·간격은 `index.html` 상단 `:root` 블록에 모여 있습니다. 포인트 컬러를 바꾸려면
`--accent`(민트) / `--accent-2`(블루) 두 값만 수정하면 사이트 전체에 반영됩니다.

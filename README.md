# 푸른노무법인 홈페이지

**이 저장소는 손으로 고치지 마십시오.** 푸른ERP 「홈페이지 관리」 화면에서
「홈페이지에 올리기」를 누르면 여기 파일이 갈아 끼워집니다 — 손으로 고친 것은 덮입니다.

## 어떻게 도나

```
푸른ERP 홈페이지 관리 화면
   └ 「홈페이지에 올리기」
        └ 서버(publishSite)가 이 저장소에 파일을 올린다
             └ GitHub Pages 가 1~2분 뒤 홈페이지에 반영한다
```

만드는 «몸통»은 푸른ERP 저장소(`nabaho/pureunall`)에 있습니다.

| 하는 일 | 어디에 |
|---|---|
| 구성원 카드 그리기 | `js/pu-site-people.js` |
| 쪽 본문 줄 갈아 끼우기 | `js/pu-site-page.js` |
| 자문사 로고·메인 띠 | `js/pu-site-partner.js` |
| 처음 굳히기(지금 홈페이지 떠 오기) | `scripts/freeze-homepage.js` |
| 올려 주는 서버 | `functions/site-publish.js` |

## 주소

쪽마다 `<이름>/index.html` 입니다. 도메인을 옮겨도 `/people`·`/work1` 이 그대로
살아야 검색(네이버·구글) 노출이 안 끊깁니다. 링크는 모두 **상대 주소**라
어느 자리에 두어도 그대로 돕니다.

## 아직 미리보기입니다

지금은 검색에 안 잡히게 막아 두었습니다(`noindex`). 도메인을 옮길 때
`node scripts/freeze-homepage.js --live` 로 다시 굳히면 그 막음이 빠집니다.

# GitHub README 동적 통계 옵션들

## 1. 미니멀 스타일 (현재 적용된 것)

```markdown
![](https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&theme=default&hide_border=true&hide_title=true&count_private=true&hide=contribs&line_height=20&text_color=333&icon_color=333)
```

## 2. 컴팩트한 통계들

### 스트릭 (연속 커밋)
```markdown
![](https://github-readme-streak-stats.herokuapp.com/?user=USERNAME&theme=default&hide_border=true&date_format=%5BY.%5Dn.j&stroke=333333&ring=333333&fire=333333&currStreakLabel=333333)
```

### WakaTime 통계 (코딩 시간 추적 - WakaTime 계정 필요)
```markdown
![](https://github-readme-stats.vercel.app/api/wakatime?username=USERNAME&theme=default&hide_border=true&hide_title=true&layout=compact)
```

## 3. 텍스트 기반 통계

### 프로필 요약 (텍스트만)
```markdown
![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=USERNAME&theme=default)
```

### 트로피 (미니멀 버전)
```markdown
![](https://github-profile-trophy.vercel.app/?username=USERNAME&theme=flat&no-frame=true&no-bg=true&margin-w=4&margin-h=4&column=7)
```

## 4. 아주 미니멀한 옵션

### 단순 커밋 카운트
```markdown
![](https://img.shields.io/badge/dynamic/json?color=lightgray&label=commits&query=%24.total_commits&url=https%3A%2F%2Fapi.github.com%2Fsearch%2Fcommits%3Fq%3Dauthor%3AUSERNAME)
```

### 단순 저장소 개수
```markdown
![](https://img.shields.io/badge/dynamic/json?color=lightgray&label=repos&query=%24.public_repos&url=https%3A%2F%2Fapi.github.com%2Fusers%2FUSERNAME)
```

## 5. 애니메이션 통계 (선택사항)

### 기여도 뱀 (contribution snake)
```markdown
![](https://raw.githubusercontent.com/USERNAME/USERNAME/output/github-contribution-grid-snake.svg)
```
(참고: 이건 GitHub Actions 설정이 필요합니다)

## 6. 커스텀 색상 팁

미니멀한 느낌을 위한 색상 옵션들:
- `&text_color=333333` - 진한 회색 텍스트
- `&bg_color=ffffff` - 흰 배경
- `&hide_border=true` - 테두리 제거
- `&title_color=333333` - 제목 색상
- `&icon_color=666666` - 아이콘 색상

## 7. 레이아웃 옵션

```markdown
<!-- 나란히 배치 -->
<a href="#">
  <img align="center" src="https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&theme=default&hide_border=true" />
</a>
<a href="#">
  <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=USERNAME&layout=compact&theme=default&hide_border=true" />
</a>
``` 
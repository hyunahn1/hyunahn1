# 🚀 GitHub Profile 자동화 설정 가이드

## 📋 준비사항
- GitHub 계정 (`hyunahn1`)
- `hyunahn1/hyunahn1` 이름의 퍼블릭 저장소 생성 필요

---

## ⚡ 1단계: 저장소 생성 및 업로드

### 1. GitHub에서 새 저장소 생성
- GitHub.com → 우측 상단 `+` → `New repository`
- 저장소 이름: **hyunahn1** (사용자명과 동일)
- 반드시 **Public**으로 설정
- README 추가하지 말기 (이미 있으니까)
- `Create repository` 클릭

### 2. 파일 업로드
```bash
# 현재 폴더에서 Git 초기화
git init
git add .
git commit -m "✨ Initial commit: Awesome profile setup"

# GitHub 저장소와 연결
git remote add origin https://github.com/hyunahn1/hyunahn1.git
git branch -M main
git push -u origin main
```

---

## 🔧 2단계: GitHub Actions 권한 설정

### 1. 저장소 Settings로 이동
`https://github.com/hyunahn1/hyunahn1` → `Settings` → `Actions` → `General`

### 2. 권한 설정 변경
- **Workflow permissions** 섹션에서
- **"Read and write permissions"** 선택
- **"Allow GitHub Actions to create and approve pull requests"** 체크
- **Save** 클릭

---

## 🤖 3단계: 자동화 테스트

### 1. Actions 탭에서 확인
- `https://github.com/hyunahn1/hyunahn1/actions`
- "Update README" 워크플로우가 있는지 확인

### 2. 수동으로 실행해보기
- 워크플로우 클릭 → `Run workflow` → `Run workflow`
- 1-2분 후 README가 업데이트되었는지 확인

---

## 📊 4단계: WakaTime 설정 (선택사항)

코딩 시간 통계를 보고 싶다면:

### 1. WakaTime 계정 생성
- [wakatime.com](https://wakatime.com) 가입
- VS Code에 WakaTime 확장 설치
- API 키 복사

### 2. GitHub Secrets 설정
- `https://github.com/hyunahn1/hyunahn1/settings/secrets/actions`
- `New repository secret` 클릭
- Name: `WAKATIME_API_KEY`
- Value: WakaTime API 키 붙여넣기

### 3. 워크플로우 업데이트
`.github/workflows/update-readme.yml`에 추가:
```yaml
- name: Update WakaTime stats
  uses: anmol098/waka-readme-stats@master
  with:
    WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
    GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

---

## 🎯 예상 결과

### 최근 활동 (자동 업데이트)
```
⚡ Recent Activity 
1. 🎉 Merged PR #42 in awesome-project
2. 💪 Opened issue #43 in open-source-repo
3. ❗ Commented on #44 in community-project
4. 📝 Pushed 5 commits to main
5. 🌟 Starred cool-repository
```

### WakaTime 통계 (설정시)
```
📊 This Week I Spent My Time On

💬 Programming Languages: 
JavaScript   8 hrs 15 mins  ████████████░░░░  45.2% 
Python       6 hrs 20 mins  ████████░░░░░░░░  34.8% 
TypeScript   2 hrs 30 mins  ████░░░░░░░░░░░░  13.7% 
Other        1 hr 10 mins   ██░░░░░░░░░░░░░░   6.3%
```

---

## 🔄 업데이트 주기

- **매일 오전 9시** (한국시간) 자동 실행
- **새 코드 푸시할 때마다** 실행
- **수동으로도 언제든 실행 가능**

---

## ❓ 문제 해결

### 자동화가 작동하지 않는다면?
1. **저장소 이름 확인**: `hyunahn1/hyunahn1`이 맞는지
2. **권한 설정 확인**: Read and write permissions 활성화
3. **워크플로우 파일 위치**: `.github/workflows/update-readme.yml`
4. **마커 주석 확인**: `<!--START_SECTION:activity-->` 존재 여부

### 에러가 발생한다면?
- Actions 탭에서 로그 확인
- 보통 권한 문제가 대부분

---

## 🎉 완료!

이제 `https://github.com/hyunahn1` 프로필이 매일 자동으로 업데이트됩니다! 

- ✅ 실제 GitHub 활동 표시
- ✅ 미니멀한 디자인 유지  
- ✅ 자동 업데이트
- ✅ 개발자스러운 스타일

---

<sub>💡 팁: 첫 실행 후 24시간 뒤부터 정기적으로 업데이트됩니다!</sub> 
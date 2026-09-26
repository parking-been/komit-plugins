# Komit 플러그인

[Komit](https://komit.site) 사전점검에서 쓰는 Claude Code 플러그인입니다.

## komit-scan

바이브코딩으로 만든 서비스의 출시 준비 상태를 검사해 Komit에 올릴 결과 파일(`komit-result.md`)을 만듭니다.
준법·보안·결제·데이터·비용·인계·AI 잔재·기타 여덟 분류로 문제를 찾고, 코드만으로 판정할 수 없는 것은 의뢰인에게 물을 문항으로 만듭니다.

**소스 코드는 컴퓨터 밖으로 나가지 않습니다.** 검사는 내 컴퓨터의 Claude Code 안에서 돌고, Komit에는 결과 파일만 올립니다.
무엇을 검사하는지는 [`komit-scan/skills/komit-scan/`](komit-scan/skills/komit-scan/) 에서 누구나 읽을 수 있습니다.

### 설치

Claude Code에서:

```
/plugin install komit-scan --marketplace parking-been/komit-plugins
```

이전 버전의 Claude Code라면 두 줄로 나눠 입력합니다.

```
/plugin marketplace add parking-been/komit-plugins
/plugin install komit-scan@komit
```

### 검사

프로젝트 폴더에서 Komit 사전점검 화면에 나온 명령을 그대로 붙여 넣습니다.

```
/komit-scan <진단 번호> <겪은 일>
```

검사를 마치면 프로젝트 폴더에 생긴 `komit-result.md` 를 Komit에 올립니다.

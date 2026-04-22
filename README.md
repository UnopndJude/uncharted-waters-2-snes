# 대항해시대2 - SNES 버전 웹 에뮬레이터

[EmulatorJS](https://emulatorjs.org)를 사용해 브라우저에서 대항해시대2 (Uncharted Waters: New Horizons) SNES 버전을 실행합니다.

## 데모

GitHub Pages 배포 후: `https://UnopndJude.github.io/uncharted-waters-2-snes/`

## 로컬 실행

```bash
python3 -m http.server 8000
# 또는
npx serve .
```

브라우저에서 `http://localhost:8000` 접속.

## ROM 파일 준비 (중요)

**저작권 문제로 이 레포는 ROM을 포함하지 않습니다.** 본인이 정식 보유한 ROM만 사용하세요.

1. 대항해시대2 SNES ROM 파일 준비 (`.sfc` 또는 `.smc`)
2. 프로젝트 루트에 `game.sfc` 파일명으로 배치
3. `.gitignore`에 의해 git에는 커밋되지 않음 (의도적)

파일 업로드 UI도 내장되어 있어 로컬 파일을 직접 브라우저에서 불러올 수도 있습니다.

## 구조

```
.
├── index.html              # EmulatorJS 엔트리 포인트
├── game.sfc                # (로컬 전용, 커밋 안 됨) ROM 파일
└── .github/workflows/      # GitHub Pages 자동 배포
```

## 모바일 지원

EmulatorJS는 가상 게임패드를 지원하므로 모바일 브라우저에서도 플레이 가능합니다.

## 저작권

- 이 레포의 **코드** 부분은 MIT 라이선스
- **대항해시대2 (Uncharted Waters: New Horizons)** 는 Koei Tecmo의 저작물입니다
- 이 프로젝트는 교육/연구/개인 소장 목적의 에뮬레이터 프론트엔드만 제공합니다
- ROM 파일 배포는 저작권 침해입니다 — 본인 소유 파일만 로컬에서 사용하세요

## 기술 스택

- [EmulatorJS](https://emulatorjs.org) — libretro 코어의 WebAssembly 빌드 (snes9x)
- GitHub Pages — 정적 호스팅

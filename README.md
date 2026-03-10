# My Cursor Setup

**Cursor 설정 도서관** — 프로젝트별로 필요한 기술 스택만 골라서 적용할 수 있는 Cursor Agent/Rules/Skills 모음입니다.

Flutter, React 등 여러 기술을 지원하며, 진행 중인 프로젝트에 맞는 설정만 선택해서 복사해 사용합니다.

## 📚 도서관 개념

| 구분 | 설명 |
|------|------|
| **이 저장소** | 모든 Cursor 설정의 원본 (도서관) |
| **프로젝트** | 실제 개발 중인 앱/서비스 |
| **적용** | 프로젝트 타입에 맞는 설정만 골라 `.cursor`로 복사 |

```
my-cursor-setup (도서관)
    ├── common     → 모든 프로젝트 공통 (orchestrator, planner 등)
    ├── flutter    → Flutter 프로젝트 전용
    ├── react      → React 프로젝트 전용 (추가 예정)
    └── ...
```

## 🚀 포함 내용

### 공통 (common)
- **Agents**: orchestrator, planner, commitAgent, agentBuilder, deepDiscoveryAgent 등
- **Rules**: orchestrator, planner, code-style, agent-handoff 등

### Flutter
- **Agents**: featureImplementation, uiComponentBuilder, testCodeGenerator, apiIntegration 등
- **Rules**: flutter-animation, flutter-test, state-management (Provider)
- **Hooks**: Dart 파일 수정 후 자동 format

### 추가 예정
- React, Node.js 등

## 📦 프로젝트에 적용하기

### 1. 저장소 클론

```bash
git clone https://github.com/jumoooo/my-cursor-setup.git
cd my-cursor-setup
```

### 2. 프로젝트 타입에 맞는 설정 복사

[`docs/TECH_STACKS.md`](docs/TECH_STACKS.md)에서 해당 스택에 포함되는 파일 목록을 확인한 뒤 복사합니다.

**Flutter 프로젝트 예시:**

```bash
# 전체 .cursor 복사 (현재는 Flutter + common 포함)
cp -r .cursor /path/to/your-flutter-project/
```

**다른 스택 추가 후:** `docs/TECH_STACKS.md`를 참고해 해당 스택만 포함하는 방식으로 복사합니다.

### 3. Cursor Agent로 추출 (권장)

대상 프로젝트에서 이 저장소를 submodule로 추가한 뒤, Cursor에서:

```
.cursor에서 프로젝트에 맞는 것들만 빼서 구축해줘
```

→ `cursorLibraryExtract` Agent가 공통 + 프로젝트 타입별 파일만 선별하여 `.cursor_new`를 생성합니다.  
검토 후 `mv .cursor_new .cursor`로 적용하세요.

### 4. 설치 후

1. `config/project-config.template.json`을 `config/project-config.json`으로 복사 후 프로젝트에 맞게 수정
2. Cursor에서 프로젝트 열기
3. Agent가 자동으로 활성화됩니다

## 🏷️ 기술 스택별 매핑

| 파일 | 기술 스택 |
|------|----------|
| 상세 목록 | [`docs/TECH_STACKS.md`](docs/TECH_STACKS.md) 참고 |

## 🌿 브랜치

| 브랜치 | 용도 |
|--------|------|
| `main` | 안정 버전 (배포용) |
| `develop` | 개발/실험용 |

## 🏷️ 버전

- `main`: 최신 안정 버전
- `develop`: 개발 중인 변경사항
- 특정 버전: `git clone --branch v1.0.0 ...`

## 📄 라이선스

MIT

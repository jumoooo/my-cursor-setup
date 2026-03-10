# My Cursor Setup

**Cursor 설정 도서관** — 프로젝트별로 필요한 기술 스택만 골라서 적용할 수 있는 Cursor Agent/Rules/Skills 모음입니다.

Flutter, React 등 여러 기술을 지원하며, 진행 중인 프로젝트에 맞는 설정만 선택해서 복사해 사용합니다.

---

## ⚡ 빠른 시작 (3단계)

| 단계 | 내용 |
|------|------|
| 1 | 저장소 클론 또는 `.cursor` 폴더 복사 |
| 2 | 아래 2단계의 프롬프트를 Cursor 채팅에 붙여넣기 |
| 3 | 프로젝트에 맞는 `.cursor` 셋팅 완료 |

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

## 📦 프로젝트에 적용하기 (3단계)

### 1단계: 저장소 클론 또는 .cursor 복사

**방법 A — 클론 (권장)**

```bash
cd /path/to/your-project
git clone https://github.com/jumoooo/my-cursor-setup.git .cursor-config
```

**방법 B — 이미 클론한 경우**

```bash
# 이미 클론한 my-cursor-setup에서 .cursor만 프로젝트로 복사
cp -r /path/to/my-cursor-setup/.cursor /path/to/your-project/
```

> 방법 B로 복사한 경우 `.cursor`가 이미 있으므로 2단계는 생략 가능합니다. (현재는 common+Flutter 전체 포함)

### 2단계: Cursor 채팅에 아래 프롬프트 복사·붙여넣기

프로젝트를 Cursor에서 연 뒤, 채팅에 아래 내용을 **그대로 복사해서 붙여넣기** 하세요.

```
.cursor-config 폴더 안의 docs/TECH_STACKS.json을 읽고, 
프로젝트 루트 구조(pubspec.yaml, package.json 등)를 보고 프로젝트 타입을 감지한 뒤, 
공통(common)은 모두 포함하고, 감지된 프로젝트 타입에 해당하는 파일만 추가해서 
프로젝트 루트에 .cursor를 구축해줘.
```

> 💡 `.cursor-config` 대신 `my-cursor-setup` 등 다른 이름으로 클론한 경우, 프롬프트의 폴더명을 그에 맞게 수정하세요.

### 3단계: 완료

- `.cursor`가 프로젝트에 맞게 생성됩니다.
- `config/project-config.template.json`을 `config/project-config.json`으로 복사한 뒤 프로젝트에 맞게 수정하세요.
- Cursor를 다시 열면 Agent가 활성화됩니다.

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

# 기술 스택별 태그 매핑

프로젝트에 적용할 때, 어떤 파일을 포함할지 결정하는 가이드입니다.

## 태그

| 태그 | 설명 |
|------|------|
| `common` | 모든 프로젝트에 공통 (언어/프레임워크 무관) |
| `flutter` | Flutter/Dart 프로젝트 전용 |
| `react` | React 프로젝트 전용 (추가 예정) |

---

## Rules (`.cursor/rules/`)

| 파일 | 태그 | 비고 |
|------|------|------|
| orchestrator.mdc | common | |
| planner.mdc | common | |
| agent-handoff.mdc | common | |
| agent-builder.mdc | common | |
| bilingual-docs.mdc | common | |
| code-style.mdc | common | Flutter 예시 포함, 추후 분리 가능 |
| deep-discovery-agent.mdc | common | |
| env-orchestrator-architect.mdc | common | |
| flutter-animation.mdc | flutter | |
| flutter-test.mdc | flutter | |
| state-management.mdc | flutter | Provider 기반 |

---

## Agents (`.cursor/agents/`)

| 파일 | 태그 | 비고 |
|------|------|------|
| orchestrator.md | common | |
| planner.md | common | |
| commitAgent.md | common | |
| agentBuilder.md | common | |
| agentCritic.md | common | |
| deepDiscoveryAgent.md | common | |
| contentConsistencyAgent.md | common | |
| envOrchestratorArchitect.md | common | |
| cursorSetup.md | common | |
| cursorLibraryExtract.md | common | 도서관→프로젝트 맞춤 추출 |
| featureImplementation.md | flutter | Flutter 전용 |
| uiComponentBuilder.md | flutter | |
| testCodeGenerator.md | flutter | Flutter Test |
| uiStyleRefiner.md | flutter | |
| apiIntegration.md | flutter | |

---

## Skills (`.cursor/skills/`)

| 폴더 | 태그 |
|------|------|
| orchestrator-skills | common |
| planner-skills | common |
| agent-builder | common |
| agent-critic | common |
| commit-agent | common |
| content-consistency | common |
| cursor-setup | common |
| cursor-library-extract | common |
| deep-discovery-agent | common |
| env-orchestrator-architect | common |
| feature-implementation | flutter |
| ui-component-builder | flutter |
| test-code-generator | flutter |
| ui-style-refiner | flutter |
| api-integration | flutter |

---

## Hooks (`.cursor/hooks/`)

| 파일 | 태그 | 비고 |
|------|------|------|
| format_dart.dart | flutter | Dart 전용 |

---

## 프로젝트별 복사 가이드

### Flutter 프로젝트

현재 `.cursor` 전체는 **common + flutter**로 구성되어 있습니다. Flutter 프로젝트에는 그대로 복사하면 됩니다.

```bash
cp -r .cursor /path/to/your-flutter-project/
```

### React 프로젝트 (추가 예정)

추가 시 `common`만 복사하고, `flutter` 관련 파일은 제외합니다.  
별도 `presets/react/` 또는 스크립트로 제공 예정입니다.

---

## 확장 방법

새 기술 스택 추가 시:

1. 이 문서에 새 태그 추가 (예: `react`)
2. 해당 태그의 Rules/Agents/Skills 작성
3. `presets/` 또는 복사 가이드 업데이트

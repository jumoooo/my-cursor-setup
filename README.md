# My Cursor Setup Flutter

Flutter 프로젝트용 Cursor Agent 설정입니다.  
orchestrator, planner, featureImplementation 등 다양한 Agent와 Rules, Skills를 포함합니다.

## 🚀 포함 내용

| 구분 | 내용 |
|------|------|
| **Agents** | orchestrator, planner, featureImplementation, uiComponentBuilder, testCodeGenerator, commitAgent 등 |
| **Rules** | code-style, orchestrator, state-management, flutter-animation, flutter-test 등 |
| **Skills** | planner-skills, feature-implementation, orchestrator-skills 등 |
| **Hooks** | Dart 파일 수정 후 자동 format |

## 📦 설치 방법

### 방법 1: 직접 복사 (가장 단순)

```bash
git clone https://github.com/jumoooo/my-cursor-setup-flutter.git
cp -r my-cursor-setup-flutter/.cursor /path/to/your-flutter-project/
```

### 방법 2: Git Submodule

```bash
cd your-flutter-project
git submodule add https://github.com/jumoooo/my-cursor-setup-flutter.git .cursor-config
cp -r .cursor-config/.cursor .cursor
```

### 방법 3: Windows (PowerShell)

```powershell
git clone https://github.com/jumoooo/my-cursor-setup-flutter.git
Copy-Item -Recurse my-cursor-setup-flutter\.cursor -Destination C:\path\to\your-project\
```

## ⚙️ 설치 후

1. `config/project-config.template.json`을 `config/project-config.json`으로 복사 후 프로젝트에 맞게 수정
2. Cursor에서 프로젝트 열기
3. Agent가 자동으로 활성화됩니다

## 🏷️ 버전

- `main`: 최신 안정 버전
- 특정 버전: `git clone --branch v1.0.0 ...`

## 📄 라이선스

MIT

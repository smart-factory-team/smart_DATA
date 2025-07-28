# smart_DATA

자동차 제조 공정 전반에서 발생할 수 있는 **설비 고장 및 품질 결함 탐지**를 위한  
AI 기반 이상탐지/예측 모델링 결과를 정리한 통합 저장소입니다.


## 🎯 목적

- 공정별 시계열/이미지 데이터를 기반으로 **이상탐지, 불량 분류, 예측 모델**을 개발
- 실제 스마트팩토리 환경을 가정하여, **현장 적용 가능성**을 고려한 모델링 수행
- 향후 **이상 대응 에이전트**, **리포트 자동화** 등 서비스 확장을 위한 기반 마련



## 📂 디렉토리 구조

```

smart_DATA/
├── press_fault_prediction/ # 프레스 - 유압펌프 고장 예측
├── press_defect_prediction/ # 프레스 - 생산품 불량 예측
├── body_welding_fault_detection/ # 차체 - 로봇 용접기 고장 탐지
├── painting_surface_defect_classification/ # 도장 - 표면 결함 이미지 분류
├── painting_equipment_anomaly_detection/ # 도장 - 설비 이상 탐지
├── assembly_component_defect_detection/ # 의장 - 부품 결함 탐지
├── agent_fault_chatbot/ # 에이전트 - 이상 대응 챗봇

```


각 폴더는 다음의 구조로 구성되어 있습니다:

```

eda/ : 데이터 탐색 및 시각화
preprocessing/ : 전처리 및 증강
model/ : 모델 정의 및 학습/평가 코드
results/ : 결과 정리 및 성능 지표
README.md : 공정별 설명

```

## ⚙️ 기술 스택

- Python 3.10+, Google Colab 기반 개발
- 주요 라이브러리: NumPy, Pandas, Scikit-learn, TensorFlow, Matplotlib
- 이미지 기반 모델은 OpenCV, Torch 사용


## 🔧 Git 브랜치 전략 및 커밋 컨벤션

본 프로젝트는 **Trunk-Based Development (TBD)** 전략을 따릅니다.  
브랜치는 단기 브랜치만 운영하며, 작업 후 빠르게 `main`에 병합합니다.

### 📌 브랜치 전략

- 기본 브랜치: `main`
- 작업 브랜치: 단기 브랜치 → PR → merge 후 삭제
- 각 브랜치는 명확한 작업 단위를 기준으로 생성

### 📄 브랜치 네이밍 규칙

형식: `<type>/<issue-number>/<short-description>`

- `type`: 작업 유형 (init, feat, fix, refactor, chore 등)
- `issue-number`: 연동된 이슈 번호
- `short-description`: 작업 요약 (kebab-case)

### 💡 브랜치 예시

```
init/1/setup-project
feat/12/add-augmentation
fix/34/fix-threshold-error
refactor/21/clean-preprocessing
chore/99/update-readme
```

## ✏️ 커밋 메시지 컨벤션

커밋 메시지는 **Gitmoji**를 사용하여 의미를 명확히 합니다.  
형식: `:gitmoji: <type>: <commit message>`

### 🗂 주요 Gitmoji 목록

| 이모지 | 코드                   | 의미           |
|--------|------------------------|----------------|
| 🎉     | `:tada:`               | 초기 커밋       |
| ✨     | `:sparkles:`           | 새 기능 추가     |
| 🐛     | `:bug:`                | 버그 수정       |
| ♻️     | `:recycle:`            | 리팩토링        |
| 🔥     | `:fire:`               | 코드/파일 제거  |
| 📝     | `:memo:`               | 문서 수정       |
| 🔧     | `:wrench:`             | 설정 파일 수정  |
| 🚑     | `:ambulance:`          | 긴급 수정       |
| ✅     | `:white_check_mark:`   | 테스트 추가     |
| 🚀     | `:rocket:`             | 배포 관련 작업  |
| 📦     | `:package:`            | 패키지 추가/변경|
| ⬆️     | `:arrow_up:`           | 패키지 업그레이드 |
| ⬇️     | `:arrow_down:`         | 패키지 다운그레이드 |


### 💡 커밋 예시

```
git commit -m "🐛 fix: correct threshold calculation logic"
git commit -m "📝 docs: add description for augmentation function"
git commit -m "♻️ refactor: split preprocessing logic into modules"
```


## 🔄 PR 가이드

- 각 작업 완료 시 PR 생성
- PR 제목은 작업 내용을 명확히 표현
- 코드 리뷰 이후 `main`으로 merge
- 긴 브랜치 유지 지양, main은 항상 배포 가능한 상태 유지


## ℹ️ 참고

- 브랜치 및 커밋 단위를 작게 유지해 충돌 방지
- GitHub Issues와 연동하여 작업 관리
- 일부 협업 도구 (Gitmoji 플러그인 등)는 프로젝트에 설정되어 있음
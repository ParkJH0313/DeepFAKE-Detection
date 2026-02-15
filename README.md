# Research Pipeline - Deepfake Detection in SNS Environment



```mermaid

%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'18px'}}}%%



timeline

    title Research Pipeline : SNS 환경 딥페이크 탐지 강건성 연구

    

    section Phase 1 - Baseline

        실험 목적 : 기본 성능 측정

        결과 : 99.3% Accuracy (Clean Images)

        기술 스택 : Xception, 140K Dataset, Transfer Learning

    

    section Phase 2 - Analysis  

        실험 목적 : SNS 환경 취약점 분석

        핵심 발견 : Gaussian Blur σ≥1.5에서 63.3%로 급락

        추가 분석 : JPEG 강건(98%+), 중앙 의존성, Instagram 취약

        인사이트 : Critical Threshold σ=1.5 발견

    

    section Phase 3 - Solution

        실험 목적 : Blur 강건성 개선

        해결 방법 : Aggressive Blur Augmentation (50%)

        최종 결과 : 90%+ 회복

        성능 향상 : +36.7%p Performance Recovery

```
# Research Pipeline - Deepfake Detection in SNS Environment

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'16px', 'cScale0':'#ffd54f', 'cScale1':'#ce93d8', 'cScale2':'#64b5f6'}}}%%

timeline
    title <b>Research Pipeline : SNS 환경 딥페이크 탐지 강건성 연구</b>
    
    section <b>Phase 1 - Baseline</b>
        <b>실험 목적</b> : 기본 성능 측정
        <b>결과</b> : 99.3% Accuracy (Clean Images)
        <b>기술 스택</b> : Xception, 140K Dataset, Transfer Learning
    
    section <b>Phase 2 - Analysis</b>
        <b>실험 목적</b> : SNS 환경 취약점 분석
        <b>핵심 발견</b> : Gaussian Blur σ≥1.5에서 63.3%로 급락
        <b>추가 분석</b> : JPEG 강건(98%+), 중앙 의존성, Instagram 취약
        <b>인사이트</b> : Critical Threshold σ=1.5 발견
    
    section <b>Phase 3 - Solution</b>
        <b>실험 목적</b> : Blur 강건성 개선
        <b>해결 방법</b> : Aggressive Blur Augmentation (50%)
        <b>최종 결과</b> : 90%+ 회복
        <b>성능 향상</b> : +36.7%p Performance Recovery
```

---

## 대안: 더 간결한 버전

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'16px', 'cScale0':'#ffca28', 'cScale1':'#ba68c8', 'cScale2':'#42a5f5'}}}%%

timeline
    title <b>Research Pipeline : SNS 환경 딥페이크 탐지 강건성 연구</b>
    
    section <b>Phase 1 - Baseline</b>
        <b>실험 목적</b> : 기본 성능 측정
        <b>결과</b> : 99.3% Accuracy
        <b>기술</b> : Xception + 140K Dataset
    
    section <b>Phase 2 - Analysis</b>
        <b>실험 목적</b> : SNS 환경 취약점 분석
        <b>핵심 발견</b> : Blur σ≥1.5 → 63.3% 급락
        <b>추가</b> : JPEG 강건 / Instagram 취약
        <b>인사이트</b> : Critical Threshold σ=1.5
    
    section <b>Phase 3 - Solution</b>
        <b>실험 목적</b> : Blur 강건성 개선
        <b>해결</b> : Aggressive Augmentation
        <b>결과</b> : 90%+ 회복 (+36.7%p)
```

---

## 대안 2: 색상만 조정한 원본

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'16px', 'cScale0':'#ffe082', 'cScale1':'#d1a3d9', 'cScale2':'#90caf9'}}}%%

timeline
    title Research Pipeline : SNS 환경 딥페이크 탐지 강건성 연구
    
    section Phase 1 - Baseline
        실험 목적 : 기본 성능 측정
        결과 : 99.3% Accuracy (Clean Images)
        기술 스택 : Xception, 140K Dataset, Transfer Learning
    
    section Phase 2 - Analysis  
        실험 목적 : SNS 환경 취약점 분석
        핵심 발견 : Gaussian Blur σ≥1.5에서 63.3%로 급락
        추가 분석 : JPEG 강건(98%+), 중앙 의존성, Instagram 취약
        인사이트 : Critical Threshold σ=1.5 발견
    
    section Phase 3 - Solution
        실험 목적 : Blur 강건성 개선
        해결 방법 : Aggressive Blur Augmentation (50%)
        최종 결과 : 90%+ 회복
        성능 향상 : +36.7%p Performance Recovery
```

---

## 설명

### 적용한 수정사항:
1. **Bold 추가**: `<b>실험 목적</b>`, `<b>결과</b>` 등 라벨에 볼드 적용
2. **보라색 연하게**: 
   - 원본: 진한 보라 → 수정: `#ce93d8` (연한 보라/라벤더)
   - 대안에서는 `#ba68c8`, `#d1a3d9` 등 다양한 옵션 제공
3. **색상 조합**:
   - Phase 1: 노란색 (`#ffd54f`, `#ffca28`, `#ffe082`)
   - Phase 2: 연한 보라 (`#ce93d8`, `#ba68c8`, `#d1a3d9`)
   - Phase 3: 파란색 (`#64b5f6`, `#42a5f5`, `#90caf9`)

### 주의사항:
Timeline 스타일의 경우 Mermaid 자체 제약으로 인해 **간격과 화살표는 기본 렌더링 방식**을 따릅니다. 안타깝게도 Mermaid timeline에서는 이를 직접 제어할 수 없습니다. 

만약 더 세밀한 커스터마이징이 필요하다면, 다른 다이어그램 타입(flowchart, graph)을 사용하거나 HTML/이미지로 만드는 것을 추천드립니다.

어떤 색상 조합이 가장 마음에 드시나요?


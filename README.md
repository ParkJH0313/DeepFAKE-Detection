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


# Research Pipeline - Deepfake Detection in SNS Environment

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'16px', 'fontFamily':'arial'}}}%%

graph LR
    subgraph P1["<b>PHASE 1</b><br/>Baseline Experiment<br/>────────────"]
        A1["<b>🎯 실험 목적</b><br/>딥페이크 탐지 기본 성능 측정<br/><br/><b>📊 결과</b><br/>Accuracy: <b>99.3%</b><br/><br/><b>🔧 사용 기술</b><br/>• Xception Model<br/>• 140K Dataset<br/>• Transfer Learning"]
    end
    
    subgraph P2["<b>PHASE 2</b><br/>Robustness Analysis<br/>────────────"]
        B1["<b>🎯 실험 목적</b><br/>SNS 환경 품질저하 영향 분석<br/><br/><b>⚠️ 핵심 발견</b><br/>Gaussian Blur σ≥1.5<br/>Accuracy: <b>63.3%</b> 급락<br/><br/><b>📌 추가 분석</b><br/>• JPEG 압축: 98%+ 유지<br/>• Spatial Masking: 중앙 의존<br/>• Instagram 시나리오 취약"]
        B2["<b>💡 인사이트</b><br/>Critical Threshold<br/><b>σ = 1.5</b><br/>실전 배포 시<br/>치명적 약점 발견"]
    end
    
    subgraph P3["<b>PHASE 3</b><br/>Solution & Enhancement<br/>────────────"]
        C1["<b>🎯 실험 목적</b><br/>Blur 강건성 개선<br/><br/><b>🚀 해결 방법</b><br/>Blur Augmentation 적용<br/><br/><b>✅ 최종 결과</b><br/>Aggressive Aug<br/>Accuracy: <b>90%+</b><br/><br/><b>📈 성능 향상</b><br/><b>+36.7%p</b> 회복"]
    end
    
    P1 ==>|"SNS 환경<br/>변형 적용"| P2
    P2 ==>|"Data<br/>Augmentation"| P3
    
    style P1 fill:#2d5016,stroke:#4caf50,stroke-width:4px,color:#fff
    style P2 fill:#8b0000,stroke:#f44336,stroke-width:4px,color:#fff
    style P3 fill:#4a148c,stroke:#9c27b0,stroke-width:4px,color:#fff
    
    style A1 fill:#ffffff,stroke:#4caf50,stroke-width:3px,color:#000
    style B1 fill:#ffffff,stroke:#f44336,stroke-width:3px,color:#000
    style B2 fill:#1565c0,stroke:#2196f3,stroke-width:3px,color:#fff
    style C1 fill:#ffffff,stroke:#9c27b0,stroke-width:3px,color:#000
```

---

## 대안 1: 더 깔끔한 세로 레이아웃

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'18px'}}}%%

flowchart TB
    A["<b>PHASE 1: Baseline Experiment</b><br/>─────────────────────<br/><br/><b>🎯 목적:</b> 기본 성능 측정<br/><br/><b>📊 Clean Images Accuracy: 99.3%</b><br/><br/>✓ Xception 전이학습<br/>✓ 140K 데이터셋<br/>✓ ImageNet pretrained weights"]
    
    B["<b>PHASE 2: Robustness Analysis</b><br/>─────────────────────<br/><br/><b>🎯 목적:</b> SNS 환경 취약점 분석<br/><br/><b>⚠️ Gaussian Blur σ≥1.5: 63.3% 급락</b><br/><br/>✓ JPEG 압축 강건 98%+<br/>⚠️ 중앙 얼굴 영역 의존성<br/>⚠️ Instagram 필터 환경 취약<br/><br/><b>💡 Critical Threshold: σ = 1.5</b>"]
    
    C["<b>PHASE 3: Solution & Enhancement</b><br/>─────────────────────<br/><br/><b>🎯 목적:</b> Blur 강건성 개선<br/><br/><b>🚀 Aggressive Augmentation: 90%+ 회복</b><br/><br/>✓ Conservative 30% 적용<br/>✓ Standard 40% 적용<br/>✓ Aggressive 50% 적용<br/><br/><b>📈 Performance Recovery: +36.7%p</b>"]
    
    A -->|"SNS 환경<br/>품질 저하 테스트"| B
    B -->|"Blur Data<br/>Augmentation"| C
    
    style A fill:#1b5e20,stroke:#4caf50,stroke-width:5px,color:#fff
    style B fill:#b71c1c,stroke:#f44336,stroke-width:5px,color:#fff
    style C fill:#4a148c,stroke:#9c27b0,stroke-width:5px,color:#fff
```

---

## 대안 2: 가장 심플하고 강렬한 버전 (추천!)

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'20px', 'primaryColor':'#1b5e20', 'primaryTextColor':'#fff', 'primaryBorderColor':'#4caf50', 'lineColor':'#333', 'secondaryColor':'#b71c1c', 'tertiaryColor':'#4a148c'}}}%%

graph LR
    A["<b>PHASE 1</b><br/>Baseline<br/>─────────<br/><br/><b>99.3%</b><br/>Clean Images<br/><br/>Xception 모델<br/>140K 데이터셋"]
    
    B["<b>PHASE 2</b><br/>분석<br/>─────────<br/><br/><b>63.3%</b><br/>Blur σ≥1.5<br/><br/>⚠️ 치명적 약점<br/>Instagram 취약"]
    
    C["<b>PHASE 3</b><br/>개선<br/>─────────<br/><br/><b>90%+</b><br/>회복 성공<br/><br/>✅ Blur Aug<br/>📈 +36.7%p"]
    
    A ==>|"SNS 환경<br/>테스트"| B
    B ==>|"Data<br/>Augmentation"| C
    
    style A fill:#1b5e20,stroke:#4caf50,stroke-width:6px,color:#fff
    style B fill:#b71c1c,stroke:#f44336,stroke-width:6px,color:#fff
    style C fill:#4a148c,stroke:#9c27b0,stroke-width:6px,color:#fff
```

---

## 대안 3: 타임라인 스타일 (매우 명확)

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
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'17px', 'fontFamily':'arial'}}}%%

graph LR
    subgraph P1["PHASE 1<br/>Baseline Experiment"]
        A1["<b>실험 목적</b><br/>딥페이크 탐지 기본 성능 측정<br/><br/><b>결과</b><br/>Accuracy: <b>99.3%</b><br/>(Clean Images)<br/><br/><b>사용 기술</b><br/>• Xception Model<br/>• 140K Dataset<br/>• Transfer Learning"]
    end
    
    subgraph P2["PHASE 2<br/>Robustness Analysis"]
        B1["<b>실험 목적</b><br/>SNS 환경 품질저하 영향 분석<br/><br/><b>핵심 발견</b><br/>Gaussian Blur σ≥1.5<br/>Accuracy: <b>63.3%</b> 급락<br/><br/><b>추가 분석</b><br/>• JPEG 압축: 98%+ 유지<br/>• Spatial Masking: 중앙 의존<br/>• Instagram 시나리오 취약"]
        B2["<b>인사이트</b><br/>Critical Threshold<br/><b>σ = 1.5</b><br/><br/>실전 배포 시<br/>치명적 약점 발견"]
    end
    
    subgraph P3["PHASE 3<br/>Solution & Enhancement"]
        C1["<b>실험 목적</b><br/>Blur 강건성 개선<br/><br/><b>해결 방법</b><br/>Blur Augmentation<br/><br/><b>최종 결과</b><br/>Accuracy: <b>90%+</b><br/><br/><b>성능 향상</b><br/><b>+36.7%p</b> 회복"]
    end
    
    P1 ==>|"SNS 환경<br/>변형 적용"| P2
    P2 ==>|"Data<br/>Augmentation"| P3
    
    style P1 fill:#1b5e20,stroke:#4caf50,stroke-width:4px,color:#fff
    style P2 fill:#8b0000,stroke:#d32f2f,stroke-width:4px,color:#fff
    style P3 fill:#4a148c,stroke:#7b1fa2,stroke-width:4px,color:#fff
    
    style A1 fill:#ffffff,stroke:#4caf50,stroke-width:2px,color:#000
    style B1 fill:#ffffff,stroke:#d32f2f,stroke-width:2px,color:#000
    style B2 fill:#1565c0,stroke:#1976d2,stroke-width:2px,color:#fff
    style C1 fill:#ffffff,stroke:#7b1fa2,stroke-width:2px,color:#000
```

---

## 더 심플한 버전 (추천!)

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'18px', 'fontFamily':'Arial, sans-serif'}}}%%

graph LR
    subgraph P1["PHASE 1<br/>Baseline Experiment"]
        direction TB
        A1["<b>실험 목적</b><br/>딥페이크 탐지 기본 성능 측정"]
        A2["<b>결과</b><br/>Accuracy: 99.3%"]
        A3["<b>사용 기술</b><br/>Xception Model<br/>140K Dataset<br/>Transfer Learning"]
        A1 --- A2 --- A3
    end
    
    subgraph P2["PHASE 2<br/>Robustness Analysis"]
        direction TB
        B1["<b>실험 목적</b><br/>SNS 환경 품질저하 영향 분석"]
        B2["<b>핵심 발견</b><br/>Gaussian Blur σ≥1.5<br/>Accuracy: 63.3% 급락"]
        B3["<b>추가 분석</b><br/>JPEG 압축: 98%+ 유지<br/>Spatial Masking: 중앙 의존<br/>Instagram 시나리오 취약"]
        B4["<b>인사이트</b><br/>Critical Threshold σ=1.5<br/>실전 배포 시 치명적 약점"]
        B1 --- B2 --- B3 --- B4
    end
    
    subgraph P3["PHASE 3<br/>Solution & Enhancement"]
        direction TB
        C1["<b>실험 목적</b><br/>Blur 강건성 개선"]
        C2["<b>해결 방법</b><br/>Blur Augmentation 적용"]
        C3["<b>최종 결과</b><br/>Accuracy: 90%+<br/>성능 향상: +36.7%p"]
        C1 --- C2 --- C3
    end
    
    P1 ==>|"SNS 환경<br/>변형 적용"| P2
    P2 ==>|"Data<br/>Augmentation"| P3
    
    style P1 fill:#1b5e20,stroke:#4caf50,stroke-width:5px,color:#fff
    style P2 fill:#8b0000,stroke:#d32f2f,stroke-width:5px,color:#fff
    style P3 fill:#4a148c,stroke:#7b1fa2,stroke-width:5px,color:#fff
    
    style A1 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style A2 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style A3 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style B1 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style B2 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style B3 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style B4 fill:#1565c0,stroke:#1976d2,stroke-width:2px,color:#fff
    style C1 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style C2 fill:#fff,stroke:#333,stroke-width:1px,color:#000
    style C3 fill:#fff,stroke:#333,stroke-width:1px,color:#000
```

---

## 가장 깔끔한 버전 (최종 추천!)

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'fontSize':'16px'}}}%%

flowchart LR
    subgraph Phase1["<b>PHASE 1</b><br/>Baseline Experiment<br/> "]
        A["실험 목적<br/>────────<br/>딥페이크 탐지<br/>기본 성능 측정<br/><br/>결과<br/>────────<br/>Accuracy: 99.3%<br/><br/>사용 기술<br/>────────<br/>Xception Model<br/>140K Dataset<br/>Transfer Learning"]
    end
    
    subgraph Phase2["<b>PHASE 2</b><br/>Robustness Analysis<br/> "]
        B["실험 목적<br/>────────<br/>SNS 환경<br/>품질저하 영향 분석<br/><br/>핵심 발견<br/>────────<br/>Gaussian Blur σ≥1.5<br/>Accuracy: 63.3% 급락<br/><br/>추가 분석<br/>────────<br/>JPEG 압축 98%+ 유지<br/>Spatial 중앙 의존<br/>Instagram 취약"]
        C["인사이트<br/>────────<br/>Critical Threshold<br/>σ = 1.5<br/><br/>실전 배포 시<br/>치명적 약점 발견"]
    end
    
    subgraph Phase3["<b>PHASE 3</b><br/>Solution & Enhancement<br/> "]
        D["실험 목적<br/>────────<br/>Blur 강건성 개선<br/><br/>해결 방법<br/>────────<br/>Blur Augmentation<br/><br/>최종 결과<br/>────────<br/>Accuracy: 90%+<br/>성능 향상: +36.7%p"]
    end
    
    Phase1 ==>|"SNS 환경<br/>변형 적용"| Phase2
    Phase2 ==>|"Data<br/>Augmentation"| Phase3
    
    style Phase1 fill:#1b5e20,stroke:#4caf50,stroke-width:5px,color:#fff
    style Phase2 fill:#8b0000,stroke:#d32f2f,stroke-width:5px,color:#fff
    style Phase3 fill:#4a148c,stroke:#7b1fa2,stroke-width:5px,color:#fff
    
    style A fill:#ffffff,stroke:#4caf50,stroke-width:3px,color:#000
    style B fill:#ffffff,stroke:#d32f2f,stroke-width:3px,color:#000
    style C fill:#1565c0,stroke:#1976d2,stroke-width:3px,color:#fff
    style D fill:#ffffff,stroke:#7b1fa2,stroke-width:3px,color:#000
```

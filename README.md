# Research Pipeline - Deepfake Detection

## 연구 파이프라인

```mermaid
graph LR
    subgraph Phase1["<b>PHASE 1: Baseline Experiment</b><br/>모델 성능 벤치마크"]
        A1["<b>Clean Images</b><br/>Accuracy: 99.3%"]
        A2["✓ Xception 모델<br/>✓ 140K 데이터셋<br/>✓ ImageNet 전이학습"]
        A1 ~~~ A2
    end
    
    subgraph Phase2["<b>PHASE 2: Robustness Analysis</b><br/>SNS 환경 취약점 분석"]
        B1["<b>Gaussian Blur σ≥1.5</b><br/>Accuracy: 63.3% ↓"]
        B2["⚠ Blur가 가장 치명적<br/>✓ JPEG 압축 강건 98%+<br/>⚠ 중앙 얼굴 영역 의존<br/>⚠ Instagram 필터 취약"]
        B3["<b>Critical Threshold</b><br/>σ = 1.5"]
        B1 ~~~ B2
        B2 ~~~ B3
    end
    
    subgraph Phase3["<b>PHASE 3: Solution & Enhancement</b><br/>강건성 개선"]
        C1["<b>Aggressive Augmentation</b><br/>Accuracy: 90%+ ↑"]
        C2["✓ 모든 blur에서 회복<br/>✓ Conservative 30%<br/>✓ Standard 40%<br/>✓ Aggressive 50%"]
        C3["<b>Performance Recovery</b><br/>+36.7%p"]
        C1 ~~~ C2
        C2 ~~~ C3
    end
    
    Phase1 ==> Phase2
    Phase2 ==> Phase3
    
    style Phase1 fill:#d4edda,stroke:#28a745,stroke-width:3px
    style Phase2 fill:#f8d7da,stroke:#d73a49,stroke-width:3px
    style Phase3 fill:#e7d4f5,stroke:#6f42c1,stroke-width:3px
    
    style A1 fill:#fff,stroke:#28a745,stroke-width:2px
    style B1 fill:#fff,stroke:#d73a49,stroke-width:2px
    style C1 fill:#fff,stroke:#6f42c1,stroke-width:2px
    
    style B3 fill:#667eea,stroke:#764ba2,stroke-width:2px,color:#fff
    style C3 fill:#11998e,stroke:#38ef7d,stroke-width:2px,color:#fff
```

## 사용 방법

위 코드를 GitHub README.md 파일에 그대로 복사해서 붙여넣으면 됩니다!

## 주요 특징

- ✅ **Phase 1**: Baseline 성능 (99.3%)
- ⚠️ **Phase 2**: 문제 발견 (σ≥1.5에서 63.3%로 급락)
- ✅ **Phase 3**: 해결책 적용 (90%+ 회복)

---

## Alternative: 더 간단한 버전

```mermaid
flowchart LR
    A["Phase 1: Baseline<br/>99.3% Accuracy"] 
    B["Phase 2: Analysis<br/>Blur Critical<br/>σ≥1.5 → 63.3%"]
    C["Phase 3: Solution<br/>Augmentation<br/>90%+ Recovery"]
    
    A ==>|"SNS 환경 테스트"| B
    B ==>|"Aggressive Aug"| C
    
    style A fill:#d4edda,stroke:#28a745,stroke-width:3px
    style B fill:#f8d7da,stroke:#d73a49,stroke-width:3px
    style C fill:#e7d4f5,stroke:#6f42c1,stroke-width:3px
```

## 더 간결한 버전 (추천)

```mermaid
graph LR
    A[Phase 1<br/>Baseline<br/><b>99.3%</b>] 
    B[Phase 2<br/>Analysis<br/><b>63.3%</b><br/>σ≥1.5 Critical]
    C[Phase 3<br/>Enhancement<br/><b>90%+</b><br/>+36.7%p]
    
    A -->|Robustness Test| B
    B -->|Blur Augmentation| C
    
    style A fill:#d4edda,stroke:#28a745,stroke-width:4px,color:#000
    style B fill:#f8d7da,stroke:#d73a49,stroke-width:4px,color:#000
    style C fill:#e7d4f5,stroke:#6f42c1,stroke-width:4px,color:#000
```

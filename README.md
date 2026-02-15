flowchart TD
    %% 전체 타이틀
    title["Research Pipeline : SNS 환경 딥페이크 탐지 강건성 연구"]
    style title fill:none,stroke:none,font-size:20px,font-weight:bold

    %% Phase 1
    subgraph P1 ["Phase 1 - Baseline"]
        direction TB
        P1_1("실험 목적") -.-> P1_1C["기본 성능 측정"]
        P1_2("결과") -.-> P1_2C["99.3% Accuracy (Clean Images)"]
        P1_3("기술 스택") -.-> P1_3C["Xception, 140K Dataset, Transfer Learning"]
    end

    %% Phase 2
    subgraph P2 ["Phase 2 - Analysis"]
        direction TB
        P2_1("실험 목적") -.-> P2_1C["SNS 환경 취약점 분석"]
        P2_2("핵심 발견") -.-> P2_2C["Gaussian Blur σ≥1.5에서 63.3%로 급락"]
        P2_3("추가 분석") -.-> P2_3C["JPEG 강건/중앙 의존성/Instagram 취약"]
        P2_4("인사이트") -.-> P2_4C["Critical Threshold σ=1.5 발견"]
    end

    %% Phase 3
    subgraph P3 ["Phase 3 - Solution"]
        direction TB
        P3_1("실험 목적") -.-> P3_1C["Blur 강건성 개선"]
        P3_2("해결 방법") -.-> P3_2C["Aggressive Blur Augmentation (50%)"]
        P3_3("최종 결과") -.-> P3_3C["90%+ 회복"]
        P3_4("성능 향상") -.-> P3_4C["+36.7%p Performance Recovery"]
    end

    %% 연결선 및 스타일
    P1 === P2 === P3

    style P1 fill:#FFF3E0,stroke:#FFB74D
    style P2 fill:#F3E5F5,stroke:#BA68C8
    style P3 fill:#E3F2FD,stroke:#64B5F6

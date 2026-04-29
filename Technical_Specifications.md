# 📐 Mechanical & Layout Constraints (물리적 규격 및 배치 표준)

## 1. Mainboard Specifications (메인보드 규격)
* **Form Factor:** M-ATX (244mm x 244mm)
    * Standard M-ATX mounting holes for universal case compatibility. (표준 M-ATX 나사 홀 위치를 준수하여 일반 케이스와 호환됩니다.)
* **PCB Layers:** 6-Layer (2.0mm Thickness, 2oz Copper)
    * High-rigidity structure for vibration suppression. (기계적 진동을 억제하기 위한 고강성 구조입니다.)
* **Slot Configuration:** Centralized **Hive Command** with 4 peripheral Honeycomb slots.

## 2. Honeycomb Module (Hex-Interposer) Standard (벌집형 모듈 표준)
모든 확장 모듈은 본 규격을 물리적 표준으로 삼아야 합니다.
* **Shape:** Regular Hexagon (정육각형)
* **Diagonal Diameter:** 60.0mm (대각선 길이)
    * Optimal space for high-end DAC chipsets and power cleaning filters. (하이엔드 칩셋 및 필터 실장을 위한 최적의 공간입니다.)
* **Stacking Height:** 4.0mm ~ 5.0mm (Mainboard to Module)
    * Ensures sufficient airflow and thermal isolation. (충분한 공기 흐름과 열 격리를 보장합니다.)

## 3. 40-Pin Hive Interface (40핀 하이브 인터페이스)
* **Connector Type:** 0.5mm Pitch Board-to-Board (BTB) 40-Pin Header
* **Signal Integrity:** 100Ω Differential pair matching for I2S/DSD/Clock signals. (I2S/DSD/클럭 신호를 위한 100Ω 차동 임피던스 매칭을 준수하십시오.)

---
*For specific adapter design strategies and pin mapping, please refer to `/Adapters/README.md`.*
*(구체적인 어댑터 설계 전략 및 핀 맵은 /Adapters/README.md를 참조하십시오.)*

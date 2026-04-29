# 📐 V16-HIVE: Mechanical & Layout Constraints

## 1. Mainboard Specifications (메인보드 규격)
* **Form Factor:** M-ATX (244mm x 244mm)
    * Standard M-ATX mounting holes for universal case compatibility.
* **PCB Layers:** 6-Layer (2.0mm Thickness, 2oz Copper)
    * High-rigidity structure for vibration suppression.
* **Slot Configuration:** Centralized **Hive Command** with 4x peripheral Honeycomb slots.

## 2. Honeycomb Module Interface (벌집형 모듈 표준)
모든 확장 모듈은 본 규격을 물리적 표준으로 삼습니다.
* **Shape:** Regular Hexagon (정육각형)
* **Diagonal Diameter:** 60.0mm
* **Stacking Height:** 4.0mm ~ 5.0mm (Mainboard to Module)
* **Connector:** 0.5mm Pitch Board-to-Board (BTB) 40-Pin Header

## 3. Signal Integrity Standard
* **Impedance:** 100Ω Differential pair matching for I2S/DSD/Clock.
* **Isolation:** Digital/Analog domains are strictly separated by physical moats.

---
*For specific adapter design strategies and pin mapping, please refer to `/Adapters/README.md`.*
*(구체적인 어댑터 설계 전략 및 핀 맵은 /Adapters/README.md를 참조하십시오.)*

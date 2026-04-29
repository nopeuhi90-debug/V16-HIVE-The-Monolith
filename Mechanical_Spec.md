🛡️ V16-HIVE Mainboard: Final Engineering Standards
1. Central Hub Architecture & No-Fly Zone
[English]
Central Zone (40x40mm): This area is a strictly designated "No-Fly Zone." It is reserved exclusively for the XMOS XU316 MCU and OCXO/TCXO clocks. No other components or traces are allowed within this perimeter.

Length Matching: All signal traces from the Central Hub to the four (4) Honeycomb slots must be routed with Equal-Length Traces. The length deviation must be kept under ±0.05mm to ensure zero-jitter synchronous data transmission across all modules.

[한국어]
중앙 구역 (40x40mm): 본 구역은 엄격히 지정된 '설계 금지 구역(No-Fly Zone)'입니다. 오직 XMOS XU316 MCU와 OCXO/TCXO 클럭만을 위해 예약되며, 이 영역 내부에는 어떠한 타 부품이나 배선도 허용되지 않습니다.

등장 배선 (Length Matching): 중앙 허브에서 4개의 벌집 슬롯으로 연결되는 모든 신호선은 반드시 동거리 배선이어야 합니다. 모든 모듈 간의 제로 지터(Zero-Jitter) 동기 데이터 전송을 보장하기 위해 배선 길이 오차는 ±0.05mm 이내로 제한됩니다.

## 2. Honeycomb Module Interface (벌집형 모듈 표준)
모든 확장 모듈은 본 규격을 물리적 표준으로 삼습니다.
* **Shape:** Regular Hexagon (정육각형)
* **Diagonal Diameter:** 60.0mm
* **Stacking Height:** 4.0mm ~ 5.0mm (Mainboard to Module)
* **Connector:** 0.5mm Pitch Board-to-Board (BTB) 40-Pin Header

3. Advanced Signal Integrity & Connectivity
[English]
Connector Specification: The mainboard must be equipped with 0.5mm Pitch Female (Receptacle) BTB Connectors.

Impedance Standard: The 16-Lane UHI (Universal Honeycomb Interface) requires a 100Ω Differential Impedance standard. Traces must be routed as differential pairs with consistent spacing.

Stacking Precision: The vertical distance between the mainboard surface and the adapter PCB must be maintained at exactly 4.0mm. Any deviation beyond ±0.1mm will result in mechanical failure or signal degradation.

[한국어]
커넥터 규격: 메인보드에는 반드시 0.5mm 피치 암놈(Receptacle) BTB 커넥터를 실장해야 합니다.

임피던스 표준: 16레인 UHI(Universal Honeycomb Interface)는 100Ω 차동 임피던스 표준을 요구합니다. 배선은 반드시 일정한 간격을 유지하는 차동 페어(Differential Pairs)로 구성되어야 합니다.

적층 정밀도: 메인보드 표면과 어댑터 PCB 사이의 수직 거리는 정확히 4.0mm로 유지되어야 합니다. ±0.1mm 이상의 오차는 기계적 결합 실패 또는 신호 열화를 초래합니다.

---
*For specific adapter design strategies and pin mapping, please refer to `/Adapters/README.md`.*
*(구체적인 어댑터 설계 전략 및 핀 맵은 /Adapters/README.md를 참조하십시오.)*

## 📋 V16-HIVE Technical Specifications

### 1. Performance Target
- **SNR:** -142dB (Monolith Mode)
- **THD+N:** 0.00008% @1kHz
- **DNR:** 140dB+
- **Clock Jitter:** <5ps RMS (Si5341 based)

### 2. Core Components
- **MCU:** XMOS XU316 (16-Core)
- **DAC:** 4x ESS Sabre ES9039Pro (Quad-Parallel)
- **Power:** 32x ADI LT3045 Parallel Array (Ultra-low noise)
- **Clock:** Si5341 Precision Clock Multiplier

## 3. Engineering Guidelines (제작 지침서)

본 프로젝트에 기여하거나 실제 구현을 시도하는 엔지니어는 다음 설계 지침을 반드시 준수해야 합니다.

### 📐 Signal Integrity (신호 무결성)
- **Trace Matching:** 모든 I2S 및 MCLK 배선은 ±0.001mm 이내의 등길이 배선(Serpentine Routing)을 원칙으로 합니다.
- **Impedance:** 고속 데이터 라인은 50Ω Single-ended, 100Ω Differential 임피던스를 유지하십시오.
- **Layer Stackup:** 6층 기판 설계를 권장하며, L2와 L5는 반드시 GND Plane으로 할당하여 EMI를 차단하십시오.

### ⚡ Power Purity (전원 순수성)
- **LDO Placement:** LT3045 레귤레이터는 각 DAC 코어 및 부하(Load) 지점에서 5mm 이내에 배치하여 전압 강하를 최소화하십시오.
- **Capacitor Hybrid:** Nichicon Fine Gold(전해)와 WIMA(필름) 커패시터를 혼용하여 가청 주파수 전역의 노이즈를 필터링하십시오.

### 🐝 Modular Compatibility (모듈 호환성)
- **Honeycomb Slot:** 모든 확장 카드는 V16-HIVE 40-Pin 표준 핀 맵(Pinout_Standard.md 참조)을 따라야 합니다.
- **Form Factor:** 확장 모듈의 물리적 규격은 메인보드 간섭을 방지하기 위해 정육각형(45mm x 45mm) 규격을 준수하십시오.
